<script>
	export let href = '';
	export let lang = 'en'; // the currently active language: 'en' or 'fr'
</script>

<div class="lang-toggle">
	{#if lang === 'en'}
		<span class="option active">English</span>
		<span class="divider">/</span>
		<a class="option inactive" {href} data-sveltekit-reload>Français</a>
	{:else}
		<a class="option inactive" {href} data-sveltekit-reload>English</a>
		<span class="divider">/</span>
		<span class="option active">Français</span>
	{/if}
</div>

<style>
	.lang-toggle {
		position: fixed;
		top: 4rem;
		right: 4rem;
		z-index: 100;
		display: flex;
		align-items: center;
		gap: 0.6rem;
		padding: 1rem 2rem;
		border-radius: 999px;
		background-color: rgba(255, 255, 255, 0.85);
		font-family: PoppinsSemiBold;
		font-size: 3rem;
		letter-spacing: 0.05em;
	}

	.option {
		color: black;
		text-decoration: none;
	}

	.divider {
		color: black;
		opacity: 0.3;
	}

	.active {
		opacity: 1;
	}

	.inactive {
		opacity: 0.4;
		transition: opacity 200ms ease;
	}

	.inactive:hover {
		opacity: 0.8;
	}
</style>
