<script>
	import { query_selector_all } from 'svelte/internal';
	import Toggle from './Darkmode.svelte';
	import '../app.css';
	import Footer from './Footer.svelte';
	import { onMount } from 'svelte';

	let isPageLoaded = false;

	onMount(() => {
		// setTimeout(() => {
		isPageLoaded = true;
		// }, 2000);
	});
</script>

<div class="toggle">
	<Toggle>Dark/light mode</Toggle>
</div>

{#if !isPageLoaded}
	<div id="myDiv" class="loader"><img src="spinner.svg" alt="loader" /></div>
{/if}

<main>
	<slot />
</main>

<Footer />

<style>
	:global(body.dark) {
		background-color: rgb(27, 27, 27);
		color: white;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
	}

	.toggle {
		display: flex;
		justify-content: end;
		padding-right: 1rem;
	}

	@media (max-width: 650px) {
		.toggle {
			position: absolute;
			top: 0;
			right: 0;
		}
	}

	.loader {
		position: fixed;
		top: 0;
		right: 0;
		left: 0;
		bottom: 0;
		display: grid;
		place-items: center;
		z-index: 100;
		background-color: white;
	}
</style>
