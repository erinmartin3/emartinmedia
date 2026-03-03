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
			<h2 class="font-bold text-[#457996] my-5 md:mb-7 mb-4  font-fredoka uppercase md:text-5xl text-4xl text-center">
				MixFolio
			</h2>
		</div>
		<div class="mb-10 md:mx-50 mx-10">
		<p class="">
			This personal project was built in collaboration with <a href="https://jakebogan.com" class="hover:underline font-bold" target="_blank">Jake Bogan</a> as a streamlined portfolio builder designed for users who need a custom site in minutes.
			<br><br>
			We developed both the front end and back end, enabling users to create an account, input their information through a dashboard, and instantly generate a personalized portfolio. The platform allows users to select from unique themes and customize site colors to match their personal brand.
			<br><br>
			We worked closely across all aspects of development, with Jake leading animation systems and database architecture, while I led theme swapping functionality and overall portfolio structure and setup.
			<br><br>
		</p>

		<div class="">
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 "><a href="https://mixfolio.vercel.app/" target="_blank">Live Site</a></button>
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 "><a href="https://github.com/jakebogan01/mixfolio" target="_blank">GitHub Repo</a></button>
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 "><a href="https://mixfolio.vercel.app/portfolio/sample" target="_blank">Sample Portfolio</a></button>
		</div>
		</div>
	</div>
		<section class="max-w-5xl mx-auto">
			<div class="grid md:grid-cols-2 grid-cols-1 m-5 gap-4">

				<div>
				<h2 class="font-bold text-[#457996] md:mb-4 mb-4  font-fredoka uppercase md:text-2xl text-2xl text-center md:text-left">
					Dashboard
				</h2>
			<div class="h-[300px] overflow-y-auto">
					<img
						src="/img/mixfoliodashboard.jpg"
						alt="Website Design"
						class="w-full"
					/>
				</div>
				</div>
					<div>
						<h2 class="font-bold text-[#457996] md:mb-4 mb-4  font-fredoka uppercase md:text-2xl text-2xl text-center md:text-left">
							<a href="https://mixfolio.vercel.app/portfolio/sample" target="_blank">Sample Portfolio</a>
						</h2>
				<div class="h-[300px] overflow-y-auto">
					<a href="https://mixfolio.vercel.app/portfolio/sample" target="_blank"><img
						src="/img/mixfolioportfolio.jpg"
						alt="Website Design"
						class="w-full"
					/></a>
				</div>
			</div>
				</div>

			<div class="flex flex-wrap grid	grid-cols-1 md:grid-cols-2  m-5">

				<div class="md:hidden">
					<h2 class="font-bold text-[#457996] md:mb-4  font-fredoka uppercase md:text-2xl text-2xl text-center mt-3">
						Color Swap
					</h2>
					<p class="md:p-0 p-5">One of the unique elements of this portfolio site is how you can instantly change the look of your portfolio by either swapping the theme or changing the color scheme. I led the development for this tool and wanted it to be an easy user experience while also ensuring the site is still accessible.
					</p>
				</div>

			<Video src="/img/videos/mixfoliocolorswap2.mp4" autoplay muted loop controls trackSrc="mixfoliocolorswap2.mp4"/>

				<div class="hidden md:block md:pl-5">
					<h2 class="font-bold text-[#457996] md:mb-4  font-fredoka uppercase md:text-2xl text-2xl md:pt-5 text-center md:text-left mt-8">
						Color Swap
					</h2>
					<p class="md:p-0 p-5">One of the unique elements of this portfolio site is you can instantly change the look of your portfolio by either swapping the theme or changing the color scheme. I led the development for this tool and am very happy with how it came out while ensuring the site is still accessible.
					</p>
				</div>
			</div>
		</section>
	<Footer/>
</section>