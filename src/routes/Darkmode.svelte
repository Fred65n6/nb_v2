<script>
	let darkMode = false;
	function toggle() {
		darkMode = !darkMode;
		window.document.body.classList.toggle('dark');
	}
</script>

<div class="pr-4 -mt-4">
	<input type="checkbox" id="switch" on:click={toggle} /><label for="switch">
		{#if darkMode}
			Darkmode
		{:else}
			Lightmode
		{/if}</label
	>
</div>

<style>
	input[type='checkbox'] {
		height: 0;
		width: 0;
		visibility: hidden;
	}

	label {
		cursor: pointer;
		text-indent: -9999px;
		width: 60px;
		height: 30px;
		background: rgb(48, 47, 47);
		display: block;
		border-radius: 100px;
		position: relative;
	}

	label:after {
		content: '';
		position: absolute;
		top: 5px;
		left: 5px;
		width: 20px;
		height: 20px;
		border-radius: 50%;
		box-shadow: inset 28px -4px 0px 0px white;
		background: #fff;
		border-radius: 90px;
		transition: 0.3s;
	}

	input:checked + label {
		background: #e2e3e2;
	}

	input:checked + label:after {
		left: calc(100% - 5px);
		transform: translateX(-100%);
	}

	label:active:after {
		width: 40px;
	}
</style>
