<script>
	import Header from '$lib/header/Header.svelte';
</script>

<Header />

<svelte:head>
	<title>Frokostmenu</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<nav class="flex ml-8 pt-4 -mb-4" aria-label="Breadcrumb">
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
					href="frokostmenu"
					class="ml-1 text-sm font-medium text-gray-700 hover:text-gray-900 md:ml-2 dark:text-gray-400 dark:hover:text-white"
					>Frokostmenu</a
				>
			</div>
		</li>
	</ol>
</nav>

<main>
	<section class="grid gap-6 menu">
		<br />
		<h1>Frokostmenu</h1>
		<br />

		<h2>Smørrebrød</h2>

		<h3>Sildeplatte DKK 155,-</h3>

		<p>3 forskellige slags sild, æg og ost m/ kommen</p>

		<p>
			Hjemmelavet snaps <br />
			Spørg tjeneren om dagens udvalg <br />
			<span>5cl | DKK 60,-</span>
		</p>
		<br />
		<h2>Madder</h2>
		<p>
			Kartoffelmad <br />
			Friskost fra Søtofte mejeri, urter og råsyltede rødbede <br /> <span> DKK 85,-</span>
		</p>
		<p>
			Æggesalat <br />
			Skalotteløg, purløg, tomat/avocado mayo, friteret løg <br /> <span>DKK 95,-</span>
		</p>
		<p>
			Norrøna matjes sild<br />
			Creme på Høgelundgaards blå skimmelost, rødløg, urter <br /> <span>DKK 95,-</span>
		</p>
		<p>
			Solbær sild <br />
			Kapers, creme fraiche, æg <br /><span>DKK 95,-</span>
		</p>
		<p>Senneps sild <br /> <span>DKK 95,-</span></p>
		<p>
			Friteret torsk<br />
			Karamelliseret løg, remoulade, urter <br /> <span>DKK 115,-</span>
		</p>
		<p>
			Roastbeef <br />
			Brunet smør vinaigrette, sauerkraut, urter <br /><span>DKK 95,-</span>
		</p>
		<p>Svinekæbe <br /> Peberrodscreme, syltet løg <br /><span>DKK 105,-</span></p>
		<p>
			Rejesalat <br />
			Skagen mayo, dill, peberrod og ørredrogn på smørristet sandwichbrød <br /><span
				>DKK 125,-</span
			>
		</p>
		<p>
			Hønsesalat <br />
			Grøn asparges, "flæskesvær" og råsyltet rabarber <br /><span>DKK 105,-</span>
		</p>
		<br />
		<h2>Desserter</h2>
		<p>
			Lille mandelkage <br />
			M/ flødeskum <br /><span>DKK 45,-</span>
		</p>
		<p>
			Cheesecake <br />
			M/ hvid chokolade <br /><span> DKK 95,-</span>
		</p>
		<p>
			Marengs <br />
			M/ lemon curd, fløde, danske jordbær & vaniljeis <br /><span>DKK 105,-</span>
		</p>
	</section>
</main>

<style>
	main {
		background-image: url('../../static/shop_bg.svg');
		background-size: auto;
		background-position: top;
	}

	.menu {
		padding-inline: 1rem;
		display: grid;
		place-items: center;
		text-align: center;
		max-width: 600px;
		margin: 0 auto;
	}

	span {
		font-style: italic;
	}
</style>
