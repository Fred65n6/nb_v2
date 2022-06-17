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

<section class="main">
	<div class="book grid md:grid-cols-2">
		<div class="image">
			<img src="book_bord.webp" alt="mad fra nørrebrobryghus" />
		</div>
		<div class="mobil_img"><img src="book_bord.mobile.webp" alt="mad fra nørrebro bryghus" /></div>
		<div class="">
			<div class=" grid place-items-center gap-2 pt-12">
				<h1>Book bord her</h1>
				<p class="-mt-4 mb-4">Få din næste oplevelse hos os</p>
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
	h1, h2, p {
		color: var(--text-white);
	}
	.main {
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
		width: var(--card-width);
		height: var(--card-height);
		background-image: url('../../static/aftenmenu.webp');
		background-image: url('aftenmenu.webp');
		background-size: contain;
		padding: var(--card-padding);
		padding-top: var(--card-p-padding-top);
	}
	.card_2 {
		width: var(--card-width);
		height: var(--card-height);
		background-image: url('../../static/frokostmenu.webp');
		background-image: url('frokostmenu.webp');
		background-size: contain;
		padding: var(--card-padding);
		padding-top: var(--card-p-padding-top);
	}
	.card_3 {
		width: var(--card-width);
		height: var(--card-height);
		background-image: url('../../static/olsortiment.webp');
		background-image: url('olsortiment.webp');
		background-size: contain;
		background-repeat: no-repeat;
		padding: var(--card-padding);
		padding-top: var(--card-p-padding-top);
	}

	.menuer {
		padding-top: var(--section-general-padding);
	}

	@media (max-width: 400px) {
		.book {
			width: 19em;
			display: grid;
			place-items: center;
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
