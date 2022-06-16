<script>
	let current = '';
	import Button_white from './Button_white.svelte';
	import Button_black from './Button_blacks.svelte';
</script>

<div class={current === 'cookie' ? 'selected' : ''} on:click={() => (current = 'cookie')}>
	<div class="scale-in-ver-bottom md:w-[60rem] w-[25rem]  z-50 cookie">
		<div class="container py-12 px-8 mr-8 bg-slate-100 shadow-2xl ">
			<div class="flex place-content-end pb-8">
				<button
					class={current === 'cookie' ? 'selected' : ''}
					on:click={() => (current = 'cookie')}
				>
					<div class="close">
						<svg
							xmlns="http://www.w3.org/2000/svg"
							xmlns:xlink="http://www.w3.org/1999/xlink"
							aria-hidden="true"
							role="img"
							class="iconify iconify--carbon"
							width="32"
							height="32"
							preserveAspectRatio="xMidYMid meet"
							viewBox="0 0 32 32"
							><path
								fill="#888888"
								d="M16 2C8.2 2 2 8.2 2 16s6.2 14 14 14s14-6.2 14-14S23.8 2 16 2zm5.4 21L16 17.6L10.6 23L9 21.4l5.4-5.4L9 10.6L10.6 9l5.4 5.4L21.4 9l1.6 1.6l-5.4 5.4l5.4 5.4l-1.6 1.6z"
							/></svg
						>
					</div></button
				>
			</div>

			<div class="grid place-items-center">
				<h3 class="text-center  text-black">Tilmeld dig vores nyhedsbrev</h3>
				<p class="text-center pb-8 text-black">Og få eklusive tilbud direkte ind på din mail</p>
				<div class="md:flex grid gap-4 pt-4">
					<input
						class="h-[45px] w-[220px] border-2 p-2"
						placeholder="Eks. lars.larsen@gmail.com"
						type="Email"
					/>
					<button
						class={current === 'cookie' ? 'selected' : ''}
						on:click={() => (current = 'cookie')}
					>
						<Button_black>Tilmeld</Button_black></button
					>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	button {
		display: block;
	}

	.selected {
		display: none;
	}

	.cookie {
		position: fixed;
		left: 0;
		right: 0;
		margin-left: auto;
		margin-right: auto;
		padding-top: 8rem;
		z-index: 150;
	}

	.container {
		background-image: url('../../static/shop_bg.svg');
		background-size: auto;
		background-position: top;
	}
</style>
