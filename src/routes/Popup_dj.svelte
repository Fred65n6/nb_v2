<script context="module" lang="ts">
	let onTop; //keeping track of which open modal is on top
	const modals = {}; //all modals get registered here for easy future access

	// 	returns an object for the modal specified by `id`, which contains the API functions (`open` and `close` )
	export function getModalDj(id = '') {
		return modals[id];
	}
</script>

<script lang="ts">
	import { onDestroy } from 'svelte';
	import ButtonBlack from './Button_blacks.svelte';
	let topDiv;
	let visible = false;
	let prevOnTop;
	let closeCallback;

	export let id = '';

	function keyPress(ev) {
		//only respond if the current modal is the top one
		if (ev.key == 'Escape' && onTop == topDiv) close(); //ESC
	}

	/**  API **/
	function open(callback) {
		closeCallback = callback;
		if (visible) return;
		prevOnTop = onTop;
		onTop = topDiv;
		window.addEventListener('keydown', keyPress);

		//this prevents scrolling of the main window on larger screens
		document.body.style.overflow = 'hidden';

		visible = true;
		//Move the modal in the DOM to be the last child of <BODY> so that it can be on top of everything
		document.body.appendChild(topDiv);
	}

	function close(retVal) {
		if (!visible) return;
		window.removeEventListener('keydown', keyPress);
		onTop = prevOnTop;
		if (onTop == null) document.body.style.overflow = '';
		visible = false;
		if (closeCallback) closeCallback(retVal);
	}

	//expose the API
	modals[id] = { open, close };

	onDestroy(() => {
		delete modals[id];
		window.removeEventListener('keydown', keyPress);
	});
</script>

<div id="topModal" class:visible bind:this={topDiv} on:click={() => close()}>
	<div id="modal" on:click|stopPropagation={() => {}}>
		<svg id="close" on:click={() => close()} viewBox="0 0 12 12">
			<circle cx="6" cy="6" r="6" />
			<line x1="3" y1="3" x2="9" y2="9" />
			<line x1="9" y1="3" x2="3" y2="9" />
		</svg>
		<div id="modal-content">
			<slot />
			<div class="mx-4 pb-4">
				<ButtonBlack>Book Nu</ButtonBlack>
			</div>
		</div>
	</div>
</div>

<style>
	#topModal {
		visibility: hidden;
		z-index: 9999;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background: var(--event-popup-bg-color);
		display: flex;
		align-items: center;
		justify-content: center;
	}
	#modal {
		max-width: var(--event-popup-max-width);
		position: relative;
		background: var(--generel-bg-white);
		filter: var(--event-popup-drop-shadow);
	}

	.visible {
		visibility: visible !important;
	}

	#close {
		position: absolute;
		top: var(--close-button-top);
		right: var(--close-button-right);
		width: var(--close-button-width);
		height: var(--close-button-height);
		cursor: pointer;
		fill: var(--close-button-color);
		transition: var(--close-button-transform);
	}

	#close:hover {
		transform: scale(2);
	}

	#close line {
		stroke: #fff;
		stroke-width: 2;
	}
	#modal-content {
		color: var(--text-black);
		max-width: calc(100vw - 20px);
		max-height: calc(100vh - 20px);
		overflow: auto;
	}
</style>
