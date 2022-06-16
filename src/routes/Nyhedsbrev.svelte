<script>
	let current = '';
	import Button_white from './Button_white.svelte';
</script>

<div class={current === 'cookie' ? 'selected' : ''} on:click={() => (current = 'cookie')}>
	<div class="absolute scale-in-ver-bottom md:w-[60rem] w-[25rem]  z-50 cookie">
		<div class="p-20 mb-4 mr-8 bg-black/90 ">
			<div class="flex place-content-end">
				<button
					class={current === 'cookie' ? 'selected' : ''}
					on:click={() => (current = 'cookie')}
				>
					<Button_white>X</Button_white></button
				>
			</div>

			<div class="grid place-items-center">
				<h3 class="text-center  text-white">Tilmeld dig vores nyhedsbrev</h3>
				<p class="text-center pb-8 text-white">Og få eklusive tilbud direkte ind på din mail</p>
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
						<Button_white>Tilmeld</Button_white></button
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
		position: absolute;
		left: 0;
		right: 0;
		margin-left: auto;
		margin-right: auto;
	}
</style>
