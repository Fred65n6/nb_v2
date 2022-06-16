<script>
	// @ts-nocheck
	import Header from '$lib/header/Header.svelte';
	import ButtonWhite from './Button_white.svelte';
	import Button_white from './Button_white.svelte';
	import Form from './Form.svelte';
	import ProgressBar from './ProgressBar.svelte';
	let steps = ['1', '2', '3', '4'],
		currentActive = 1,
		progressBar;

	const handleProgress = (stepIncrement) => {
		progressBar.handleProgress(stepIncrement);
	};
</script>

<Header />

<svelte:head>
	<title>Book bord</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<nav class="flex md:ml-8 ml-4 pt-4 mb-4" aria-label="Breadcrumb">
	<ol class="inline-flex items-center space-x-1 md:space-x-3">
		<li class="inline-flex items-center">
			<a
				href="/"
				class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white"
			>
				<svg
					class="mr-2 w-4 h-4"
					fill="currentColor"
					viewBox="0 0 20 20"
					xmlns="http://www.w3.org/2000/svg"
					><path
						d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
					/></svg
				>
				Home
			</a>
		</li>
		<li>
			<div class="flex items-center">
				<svg
					class="w-6 h-6 text-gray-400"
					fill="currentColor"
					viewBox="0 0 20 20"
					xmlns="http://www.w3.org/2000/svg"
					><path
						fill-rule="evenodd"
						d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
						clip-rule="evenodd"
					/></svg
				>
				<a
					href="shop"
					class="ml-1 text-sm font-medium text-gray-700 hover:text-gray-900 md:ml-2 dark:text-gray-400 dark:hover:text-white"
					>Book bord</a
				>
			</div>
		</li>
	</ol>
</nav>

<section class="main">
	<div class="book grid md:grid-cols-2">
		<div class="image">
			<img src="book_bord.webp" alt="mad fra nørrebrobryghus" />
		</div>
		<div class="mobil_img"><img src="book_bord.mobile.webp" alt="mad fra nørrebro bryghus" /></div>
		<div class="">
			<div class=" grid place-items-center gap-2 pt-12">
				<h1 class="text-white">Book bord her</h1>
				<p class="text-white -mt-4 mb-4">Få din næste oplevelse hos os</p>
				<div class="hidden"><ProgressBar {steps} bind:currentActive bind:this={progressBar} /></div>

				<Form active_step={steps[currentActive - 1]} />

				<div class="step-button">
					<button
						class="btn"
						on:click={() => handleProgress(-1)}
						disabled={(currentActive == 1, 4)}
					>
						<Button_white>Tilbage</Button_white></button
					>

					<button
						class="btn"
						on:click={() => handleProgress(+1)}
						disabled={currentActive == steps.length}><Button_white>Næste</Button_white></button
					>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="menuer grid gap-4">
	<div class="card_1">
		<h2>Se vores <br />Aftenmenu</h2>
		<br />
		<Button_white>Se aftenmenu her</Button_white>
	</div>
	<div class="card_2">
		<h2>Se vores <br />frokostmenu</h2>
		<br />
		<Button_white>Se frokostmenu her</Button_white>
	</div>
	<div class="card_3">
		<h2>Se vores <br />Ølsortiment</h2>
		<br />
		<Button_white>Se Ølsortiment her</Button_white>
	</div>
</section>

<style>
	.main {
		font-family: 'Muli', sans-serif;
		display: grid;
		overflow: hidden;
		margin: 0 auto;
		width: 100%;
		background-color: #6e0b20;
	}

	.book {
		width: 100%;
	}

	.step-button {
		display: flex;
		gap: 20px;
		margin-top: 1rem;
		text-align: center;
	}

	.btn:disabled {
		display: none;
	}

	.card_1 {
		width: 28rem;
		height: 28rem;
		background-image: url('../../static/aftenmenu.webp');
		/* background-image: url('aftenmenu.webp'); */
		background-size: contain;
		padding: 1rem;
		padding-top: 15rem;
	}
	.card_2 {
		width: 28rem;
		height: 28rem;
		background-image: url('../../static/frokostmenu.webp');
		/* background-image: url('frokostmenu.webp'); */
		background-size: contain;
		padding: 1rem;
		padding-top: 15rem;
	}
	.card_3 {
		width: 28rem;
		height: 28rem;
		background-image: url('../../static/olsortiment.webp');
		/* background-image: url('olsortiment.webp'); */
		background-size: contain;
		background-repeat: no-repeat;
		padding: 1rem;
		padding-top: 15rem;
	}

	.menuer {
		padding-top: 3rem;
	}

	@media (max-width: 400px) {
		.book {
			width: 19em;
			display: grid;
			place-items: center;
		}

		.card_1,
		.card_2,
		.card_3 {
			width: 18em;
			height: 18em;
			padding-top: 8rem;
		}

		.mobil_img {
			width: 18em;
		}
	}

	@media (max-width: 600px) {
		.image {
			display: none;
		}
	}

	@media (min-width: 600px) {
		.book {
			height: 25rem;
			grid-template-columns: 1fr 1fr;
		}

		.image {
			width: 55rem;
			transform: scaleX(-1);
		}

		.mobil_img {
			display: none;
		}

		.menuer {
			display: flex;
			justify-content: space-between;
		}
	}
</style>
