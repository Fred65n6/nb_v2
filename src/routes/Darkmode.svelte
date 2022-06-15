<script>
	let darkMode = false;
	function toggle() {
		darkMode = !darkMode;
		window.document.body.classList.toggle('dark');
	}
</script>

<button on:click={toggle}>
	{#if darkMode}
		Darkmode
	{:else}
		Lightmode
	{/if}
</button>

<style>
	button {
		background: var(--bg-color);
		border: 2px solid var(--text-color);
		border-radius: 5px;
		color: var(--text-color);
		padding: 10px 15px;
	}

	button:active {
		background: inherit;
	}
</style>
