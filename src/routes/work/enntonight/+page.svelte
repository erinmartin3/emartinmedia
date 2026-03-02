<script>
	import Footer from '../../../components/Footer.svelte';
	import NavBar from '../../../components/NavBar.svelte';
	import { Video } from "flowbite-svelte";
	import { Lightbox } from 'svelte-lightbox';

		const gifs = [
		{ src: "/img/enntonight/enntonight.mp4", title: "PACKAGE INTRO"},
		{ src: "/img/enntonight/realshowopen.mp4", title: "LOWER THIRD"},
		{ src: "/img/enntonight/breakingnews.mp4", title: "LOOPING LOGO"},
			{ src: "/img/enntonight/ots.mp4", title: "PACKAGE INTRO"},
			{ src: "/img/enntonight/lowerthird.mp4", title: "LOWER THIRD"},
			{ src: "/img/enntonight/social.mp4", title: "PACKAGE INTRO"},
			{ src: "/img/enntonight/weatherintro.mp4", title: "LOOPING LOGO"},
			{ src: "/img/enntonight/baseball.mp4", title: "LOOPING LOGO"},
			{ src: "/img/enntonight/justweather.mp4", title: "LOWER THIRD"},
		];

	const gifs2 = [
		{ src: "/img/enntonight/linebts2.mp4", title: "PACKAGE INTRO"},
		{ src: "/img/enntonight/weatherbts2.mp4", title: "LOWER THIRD"},
		{ src: "/img/enntonight/sportsbts2.mp4", title: "LOOPING LOGO"},
		{ src: "/img/enntonight/creditline2.mp4", title: "PACKAGE INTRO"},
	];

</script>

<section class="bg-gray-100">

	<NavBar/>

	<div class=" max-w-7xl mx-auto mt-6 mb-10">
		<div class="flex justify-center">
			<h2 class="font-bold text-[#457996] my-5 md:mb-7 mb-4 dark:text-white font-fredoka uppercase md:text-5xl text-4xl text-center">
				ENN TONIGHT GRAPHICS
			</h2>
		</div>
		<p class="mb-10 md:mx-50 mx-10">
			In 2024, Elon News Network underwent a full graphics package overhaul. I collaborated with motion designer <a href="https://jacoblaplante.com/" class="hover:underline font-bold">Jacob LaPlante</a> to redesign the broadcast graphics system, creating a cohesive, modern visual identity for the show.
			<br><br>
			I then implemented and integrated the complete graphics package into the Ross Video production system, ensuring seamless functionality for both live and recorded ENN broadcasts.
		</p>

		<section class="max-w-4xl mx-auto">

			<div class="grid md:grid-cols-3 grid-cols-1 mt-4 justify-items-center">

				{#each gifs as gifs}
						<Lightbox>
							<video
								class="object-cover cursor-pointer"
								muted
								loop
								autoplay
							>
								<source src={gifs.src} type="video/mp4" />
							</video>
						</Lightbox>
					{/each}

			</div>
			<h2 class="font-bold text-[#457996] my-5 md:mt-7 mb-4 dark:text-white font-fredoka uppercase md:text-3xl text-2xl text-center">
				Ross Integration
			</h2>
				<div class="flex flex-wrap grid	grid-cols-1 md:grid-cols-2 md:m-5">

					{#each gifs2 as gifs2}
						<Lightbox>
							<video
								class="object-cover cursor-pointer"
								muted
								loop
								autoplay
							>
								<source src={gifs2.src} type="video/mp4" />
							</video>
						</Lightbox>
					{/each}

				</div>

		</section>

	</div>
	<Footer/>
</section>