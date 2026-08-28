<script>

	import { onMount } from "svelte";
	import "../assets/global-styles.css";
	import ScrollAnimate from "./ScrollAnimate.svelte";
	import TitleText from "./TitleText.svelte";

	// Text Props
	export let title = '';
	export let subtitle;
	export let type = '';
	export let styleType = undefined; // overrides the sizing class derived from `type`, for translated `type` labels
	export let subtitleLineHeight = undefined;
	export let location;
	export let titleFontColour = 'var(--brandDarkBlue)';
	export let subtitleFontColour = 'var(--brandDarkBlue)';
	export let logoType = 'White';
	export let backgroundColour = 'white';
	export let secondLogo;

	let textProps = {
		title: title,
		subtitle: subtitle,
		type: type,
		styleType: styleType,
		subtitleLineHeight: subtitleLineHeight,
		location: location,
		titleFontColour: titleFontColour,
		subtitleFontColour: subtitleFontColour,
		logoType: logoType,
		secondLogo: secondLogo
	}
	
	export let bgType = 'Image'; // Image or Video 
	export let url; // background Image/Video url
	export let tintOpacity = 0;
	export let tintColour = "black";
	export let imageOpacity = 1;
	export let imageAltText = '';
	export let topOpacity = 1;
	export let videoOpacity = 1;
	export let videoSpeed = 1;      // <-- playback speed prop
	export let mobileTextPeek = false;

	let divWidth;
	let videoEl;
	
	let isMobile = false;
	
	// reactively update playback speed
	$: if (videoEl) {
		videoEl.playbackRate = videoSpeed;
	}

	onMount(() => {
		isMobile = window.innerWidth <= 500;
		
		const resizeHandler = () => {
			isMobile = window.innerWidth <= 500;
		};
		window.addEventListener('resize', resizeHandler);

		return () => window.removeEventListener('resize', resizeHandler);
	})
</script>


<div class="title-container" style="background-color: {backgroundColour}" class:video={bgType == "Video"} bind:clientWidth={divWidth} inert={topOpacity < 0.02}>

	<TitleText {...textProps}
	/>

	{#if bgType == "Video" && !mobileTextPeek}
		<ScrollAnimate colour={titleFontColour}/>
	{/if}
	
	<div class="tint-overlay"
		style:opacity={tintOpacity}
		style:background={tintColour}></div>

	{#if bgType == "Image"}
		<div
			class="background-image"
			style="
				background-image: url({url});
				opacity: {imageOpacity};
				transition: background-position 1.5s ease-in;
			"
		></div>
	{:else if bgType == "Video"}
		<video
			class="background-video"
			class:mobile-text-peek={mobileTextPeek}
			bind:this={videoEl}
			autoplay
			muted
			loop
			playsinline
			style="opacity: {videoOpacity};"
		>
			<source src={url} type="video/mp4" />
		</video>
	{/if}

	
</div>


<style>

	.title-container {
		height: 100dvh;
		width: 100dvw;
		/* background-color: white; */
		position: relative;
		margin-bottom: 0px;
		border-bottom: solid 3px white;
		display: flex;
		align-items: center;
	}

	.tint-overlay {
		position: absolute;
		height: 100%;
		width: 100%;
		z-index: 5;
	}

	.background-image {
		position: absolute;
		width: 100%;
		height: 100%;
		background-size: cover; 
		background-position: center;
		background-repeat: no-repeat;
	}

	.background-video {
		position: absolute;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	@media (max-width: 600px) {
		.mobile-text-peek {
			height: calc(100dvh - 250px);
			margin-bottom: 5px;
		}
	}

</style>