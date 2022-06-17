<script>
	import { query_selector_all } from 'svelte/internal';
	// import Toggle from './Darkmode.svelte';
	import '../app.css';
	import Footer from './Footer.svelte';
</script>

<!-- 
<div class="toggle">
	<Toggle>Dark/light mode</Toggle>
</div> -->

<main>
	<slot />
</main>

<Footer />

<style>
	:global(body.dark) {
		background-color: rgb(26, 28, 41);
		color: var(--text-white);
	}

	:global(svg.dark) {
		color: var(--text-white);
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
</style>
