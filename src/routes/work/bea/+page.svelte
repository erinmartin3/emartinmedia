<script>
	import Footer from '../../../components/Footer.svelte';
	import NavBar from '../../../components/NavBar.svelte';
	import { Video } from "flowbite-svelte";
	import { Lightbox } from 'svelte-lightbox';

	const video = [
		{ src: "/img/videos/beaopen.mp4", title: "SHOW OPEN" },
		{ src: "/img/videos/narrative.mp4", title: "FULL PACKAGE" },
		{ src: "/img/videos/credits.mp4", title: "SHOW CREDITS" }
	];

	const gifs = [
		{ src: "/img/videos/intro.mp4", title: "PACKAGE INTRO"},
		{ src: "/img/videos/lowerthird.mp4", title: "LOWER THIRD"},
		{ src: "/img/videos/looper.mp4", title: "LOOPING LOGO"}
	];

</script>

<section class="bg-gray-100">

	<NavBar/>

	<div class=" max-w-7xl mx-auto mt-6 mb-10">
		<div class="flex justify-center">
			<h2 class="font-bold text-[#457996] my-5 md:mb-7 mb-4 dark:text-white font-fredoka uppercase md:text-5xl text-4xl text-center">
				BEA Festival of Media Arts
			</h2>
		</div>
		<p class="mb-10 md:mx-50 mx-10">
			I got the opportunity to direct and design for the 2025 Broadcast Education Association Best of Festival Awards Ceremony in Las Vegas.
			<br><br>
			I led the creative and technical execution of the large-scale live event. I developed the overall visual identity for the show, designed and animated the intro sequence, lower thirds, and full graphics package to ensure a cohesive look.
		<br><br>
			Beyond design, I directed the live production on site and oversaw content and timing to deliver a seamless experience. I also edited key video elements for the ceremony, ensuring all content aligned with the creative vision.
		</p>

		<section class="max-w-4xl mx-auto">

			<div class="grid md:grid-cols-3 grid-cols-1 gap-5 mt-4 justify-items-center">

				{#each video as video}
				<div class="flex-1 min-w-[250px] max-w-sm bg-white dark:bg-gray-900 p-4 rounded-xl shadow hover:-translate-y-1 transition-transform">
					<Video src={video.src} class="object-cover" autoplay muted loop controls trackSrc="beaopen.mp4"/>

					<div class="flex items-center justify-center">
						<h3 class="mt-2 font-fredoka font-bold text-center text-lg tracking-wider dark:bg-gray-700 text-[#457996]">{video.title}</h3>
					</div>

				</div>
					{/each}
			</div>

			<div class="grid md:grid-cols-3 grid-cols-1 gap-5 mt-4 justify-items-center">

				{#each gifs as gifs}
					<div class="flex-1 min-w-[250px] max-w-sm bg-white dark:bg-gray-900 p-4 rounded-xl shadow hover:-translate-y-1 transition-transform">
						<Lightbox>
							<video
								class="object-cover cursor-pointer"
								muted
								autoplay
								loop
							>
								<source src={gifs.src} type="video/mp4" />
							</video>
						</Lightbox>
						<div class="flex items-center justify-center">
							<h3 class="mt-2 font-fredoka font-bold text-center text-lg tracking-wider dark:bg-gray-700 text-[#457996]">{gifs.title}</h3>
						</div>

					</div>
				{/each}

			</div>
			<div class="flex justify-center mt-10">
				<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="/motion" >Explore my other motion projects</a></button>
			</div>
						</section>

	</div>
	<Footer/>
</section>