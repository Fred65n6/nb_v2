<script>
	// @ts-nocheck
	import Header from '$lib/header/Header.svelte';
</script>

<Header />

<svelte:head>
	<title>Drikkemenu</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>
<main>
	<nav class="flex md:ml-8  ml-4 pt-4 -mb-4" aria-label="Breadcrumb">
		<ol class="inline-flex items-center space-x-1 md:space-x-3">
			<li class="inline-flex items-center">
				<a
					href="/"
					class="inline-flex items-center text-sm font-medium text-gray-700 hover:underline dark:text-gray-400 dark:hover:underline"
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
					Hjem
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
						href="drikkemenu"
						class="ml-1 text-sm font-medium text-gray-700 hover:underline md:ml-2 dark:text-gray-400 dark:hover:underline"
						>Drikkemenu</a
					>
				</div>
			</li>
		</ol>
	</nav>
	<section class="grid gap-4 menu">
		<br />
		<h1>øl</h1>
		<br />
		<h2>ØLMENU for DKK 275,-</h2>
		<p>Du får både Ølcocktail og 3 øl, nøje udvalgt til at matche menuen.</p>
		<br />
		<h3>Pilsnere og lager</h3>
		<p>
			Nørrebro pilsner 4,6% <br />
			Rund og let fyldig med frisk humle <br />
			<span>DKK 55 / 70,-</span>
		</p>

		<p>
			New York Lager 5,2% <br />
			Kraftig, fyldig og gylden lager <br />
			<span>DKK 60 / 75,-</span>
		</p>

		<p>
			Nørrebro classic 4.5% <br />
			Vores bud på en klassisk gylden lagerVores bud på en klassisk gylden lager <br />
			<span>DKK 55 / 70,-</span>
		</p>

		<p>
			Stan the man <br />
			Tysk inspireret pilsner fr BRAW <br />
			<span>DKK 60 / 75,-</span>
		</p>
		<br />

		<h3>IPA og venner</h3>

		<p>
			New York Lager 5,2% <br />
			Kraftig, fyldig og gylden lager <br />
			<span>DKK 60 / 75,-</span>
		</p>

		<p>
			Bombay IPA 6.5% <br />
			En kraftig øl med masser af humle. <br />
			<span>DKK 60 / 75,-</span>
		</p>

		<p>
			New england IPA 5.0%<br />
			En kraftig øl med noter aft tropiske frugter. <br />
			<span>DKK 60 / 75,-</span>
		</p>

		<p>
			Elderflower IPA 5,0%<br />

			Session IPA med hyldeblomst <br />
			<span>DKK 60 / 75,-</span>
		</p>

		<p>
			BRAW session IPA 5,0%<br />
			Session IPA fra BRAW <br />
			<span>DKK 60 / 75,-</span>
		</p>
		<br />

		<h3>Weissbier</h3>

		<p>
			Stuykman weissbier 5,0%<br />
			Klassisk og forfriskende weissbier <br />
			<span>DKK 65 / 80,-</span>
		</p>

		<p>
			Blanche 5,0%<br />
			Frisk og tørstslukkende Witbier med et hint af lime. <br />
			<span>DKK 65 / 80,-</span>
		</p>
		<br />

		<h3>Red ale</h3>

		<p>
			Ravnsborg rød 5,5%<br />
			Klassisk cremet red ale <br />
			<span>DKK 65 / 75,-</span>
		</p>
		<br />

		<h3>Sours</h3>

		<p>
			Inferøl 6,0%<br />
			Boblende, syrlig og festlig <br />
			<span>DKK 65 / 80,-</span>
		</p>

		<p>
			Inferøl Rose 5,0%<br />
			Sour med hindbær lavet med Infernal <br />
			<span>DKK 44cl dåse / 75,-</span>
		</p>
		<br />

		<h3>Cider</h3>

		<p>
			Nørrebro æblecider 5,4%<br />
			Tør og frugtig æblecider <br />
			<span>DKK 65 / 80,-</span>
		</p>

		<br />
		<h2>Cocktails</h2>

		<p>
			Passion fruit cooler<br />
			Vodka | Passion Sparkle | Passionsfrugt<br />
			<span>DKK 95,- |DKK 395,- </span>
		</p>
		<p>
			Rock and roll spritz<br />
			Vodka | Infernøl Rose IPA| Rabarber<br />
			<span>DKK 95,- |DKK 395,- </span>
		</p>

		<p>
			Sweet home nørrebro<br />
			Gin | Elderflower SIPA| Jordbær/Rabarber<br />
			<span>DKK 95,- |DKK 395,- </span>
		</p>

		<p>
			Bramble no.5<br />
			Rom | Infernøl New Sparkle | Brombær<br />
			<span>DKK 95,- |DKK 395,- </span>
		</p>
		<br />

		<h3><span>Kander DKK 395,-</span></h3>
		<br />
		<h2>VIN</h2>
		<br />
		<h3>Hvidvin</h3>
		<p>Riesling, Tyskland <br /><span>DKK 75,-/325,-</span></p>
		<p>Soave Otto, Italien <br /><span>DKK 400,-</span></p>
		<br />
		<h2>Rosé</h2>
		<p>Une fille del l'air, Frankrig<br /><span>DKK 75,-/325,-</span></p>
		<br />
		<h2>Rødvin</h2>
		<p>Reserve Pinot Noir, Østrig <br /><span>DKK 75,-/325,-</span></p>
		<p>Brachetto D’Acqui, Spumante Dolce, Italien <br /><span>DKK 75,-/325,-</span></p>
		<br />
		<h2>Diverse</h2>
		<p>Fritz kola | <span>DKK 40,-</span></p>
		<p>Fritz kola light | <span>DKK 40,-</span></p>
		<p>Fritz kola rabarber | <span>DKK 40,-</span></p>
		<p>Fritz kola citron| <span>DKK 40,-</span></p>
		<br />
		<p>Vand m/u brus | <span>DKK 20,- pr. person</span></p>
		<p>The / Kaffe | <span>DKK 35,- pr. kop</span></p>
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

	h2 {
		color: currentcolor;
	}
</style>
