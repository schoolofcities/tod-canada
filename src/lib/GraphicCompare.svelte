<script>
	
	import "../assets/global-styles.css";
	import { onMount, onDestroy } from 'svelte';
	import { fade } from 'svelte/transition';
    import Select from 'svelte-select';

    export let images = [
        { 
            svg720: "",
            svg360: "",
            caption: "",
            source: "",
            altText: "",
            buttonLabel: ""
        }
    ]; // array of objects  

	// Shared
	export let maxWidth = '';
	export let link = 'Yes'; // Yes or No
	export let maxCaptionWidth = '680px';
	export let active = 0; // Index (starting from 0) of selected image
    
	let svgWidth = 0;
	let container;
	let resizeHandler;
	let stackHeight = 0;
	let imgWidth;
	let width;
  
	// Fetch SVG content as text
	async function loadSVG(path) {
		try {
			const response = await fetch(path);
			if (!response.ok) throw new Error(`Failed to load SVG from ${path}`);
			return await response.text(); // Return the SVG content as a string
		} catch (e) {
			console.error(`Error loading SVG from ${path}:`, e);
			return '';
		}
	}
  
	async function handleVisibility() {
		width = window.innerWidth;
		svgWidth = (width >= 720) ? 720 : 360;

        const updated = await Promise.all(images.map(async (image) => {
			const path = (width >= 720) ? image.svg720 : image.svg360;
			if (!path) return image;
			const inputSVG = await loadSVG(path);
			return { ...image, inputSVG };  // new object, not a mutation
		}));

		images = updated;
	}
  

	onMount(() => {
  		window.addEventListener("resize", handleVisibility);
  		handleVisibility();
		return () => {
			window.removeEventListener("resize", handleVisibility);
		};
	});
</script>

<div
	class="img-container"
	style="max-width: {maxWidth};"
>
    {#if images.length < 6 && width > 600}
        <div class="toggle-buttons">
            {#each images as image, index}
                <button
                    class:active={active === index}
                    on:click={() => active = index}
                >
                    {image.buttonLabel}
                </button>
            {/each}
        </div>
    {:else}
		<div class="select-theme">
			<Select class="case-study-select"
			name="case-study-select" 
			inputStyles="font-weight: 600;"
			items={images.map((image, index) => ({value: index, label: image.buttonLabel}))}
			on:change={(e) => active = e.detail.value}
			value={{ value: active, label: images[active].buttonLabel }}
			searchable={false}
			clearable={false}
			containerStyles="font-family: InterRegular !important;"
				showChevron />
		</div>
    {/if}

	<!-- {#key active}
		<div class="img-container image-layer"
				style="--svg-width: {svgWidth}px;"
				transition:fade={{duration: 400}}>
			{@html images[active]?.inputSVG}
		</div>
	{/key} -->
		
	<div class="image-stack" style="height: {stackHeight}px;">
		{#each images as image, index}
			{#if index === active}
				<div class="image-layer img-container"
						style="--svg-width: {svgWidth}px;"
						in:fade={{ duration: 400 }}
						out:fade={{ duration: 400 }}
						bind:clientHeight={stackHeight}>
					{@html image?.inputSVG}
				</div>
			{/if}
		{/each}
	</div>

	<div class="caption-container" style:width="{svgWidth}px">
		<p>
            <span class="caption-text">{@html images[active].caption}</span>
            <span class="caption-source">{@html images[active].source}</span>
		</p>
	</div>

</div>

<style>
	.img-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0 auto;
		padding-top: 10px;
		padding-bottom: 0;
		margin-bottom: 30px;
	}

	.toggle-buttons {
		display: flex;
		gap: 10px;
		margin-bottom: 10px;
	}

	button {
		font-family: InterRegular;
		background: none;
		color: var(--brandGray50);
		border: 1px solid #ccc;
		padding: 6px 12px;
		cursor: pointer;
		font-size: 14px;
	}

	button.active {
		border-color: black;
		color: black;
		background-color: #faf9f8;
		font-weight: 600;
	}

	.image-stack {
		position: relative;
		height: fit-content;
	}

	.image-layer {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
	}

    .select-theme {
        --item-is-active-bg: var(--brandGray); 
		--item-is-active-color: var(--brandBlack); 
        --item-hover-bg: #ECECE5;
		--group-title-font-weight: 900;
        --list-max-height: 600px;
		--item-first-border-radius: 0;
        --list-border-radius: 0;
		--border-radius: 0;
    }

	:global(.svelte-select) {
		cursor: pointer !important; 
	}

	:global(.svelte-select input) {
		cursor: pointer !important; 
	}

    :global(.case-study-select) {
        font-family: Inter !important;
        font-size: 14px !important;
        border-radius: 0 !important;
        border-color: #000 !important;
        margin-bottom: 1rem !important;
        /* width: 210px !important; */
		width: 220px !important;
        text-align: left;
    }

	:global(.selected-item) {
		font-size: 14px !important;
		font-weight: 600;
	}

	:global(.list-item) {
		border: 1px solid #ccc;
		border-bottom: none;
	}

	:global(.item) {
		cursor: pointer !important; 
	}

	/* :global(.item.active) {
		font-weight: 600;
	} */

	a {
		display: block;
		width: 100%;
	}

	a:hover {
		opacity: 0.95;
	}
</style>
