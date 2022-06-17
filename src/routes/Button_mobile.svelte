<script>
	// @ts-nocheck
	export let link;
	import { page } from '$app/stores';
</script>

<a class="btn" href={link}>
	<slot />
</a>

<style>
	* {
		box-sizing: border-box;
	}

	.btn {
		border: var(--border-style-white);
		border-style: solid;
		font-family: var(--heading-and-button-font);
		background-color: var(--button-bg-opacity);
		text-decoration: none;
		position: relative;
		display: inline-block;
		padding-inline: 0.8rem;
		padding-block: 0.1rem;
		font-size: var(--button-font-size);
		line-height: var(--button-line-height);
		text-align: center;
		text-transform: uppercase;
		color: var(--text-white);
		cursor: pointer;
		overflow: hidden;
		transition: 1s;
	}
</style>
