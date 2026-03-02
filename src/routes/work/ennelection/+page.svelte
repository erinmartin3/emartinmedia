<script>
	import Footer from '../../../components/Footer.svelte';
	import NavBar from '../../../components/NavBar.svelte';
	import { Video } from "flowbite-svelte";
	import { Lightbox } from 'svelte-lightbox';


	const image = [
		{ src: "/img/election/liveshot1.mp4",
			type: "video",
		},
		{ src: "/img/election/fullscreenelection1.mp4",
			type: "video",
		},
		{ src: "/img/election/electionpreshow.mp4",
			type: "video",
		},
		{ src: "/img/election.png",
			type: "img",
		},
		{ src: "/img/election/phone1.png",
			type: "img",
		},
		{ src: "/img/election/social1.jfif",
			type: "img",
		},

	];

</script>

<section class="bg-gray-100">

	<NavBar/>

	<div class=" max-w-7xl mx-auto mt-6 mb-10">
		<div class="flex justify-center">
			<h2 class="font-bold text-[#457996] my-5 md:mb-7 mb-4 dark:text-white font-fredoka uppercase md:text-5xl text-4xl text-center">
				ENN 2024 ELECTION COVERAGE
			</h2>
		</div>
		<p class="mb-10 md:mx-50 mx-10">
			Ahead of the 2024 presidential election, I led the design and visual execution of Elon News Network’s election coverage. I redesigned the election logo to align with ENN’s brand guidelines and ensure consistency with the updated broadcast graphics package.
<br><br>
			I customized and expanded the on-air graphics system specifically for the election show, creating new visual elements tailored to live results coverage. Beyond broadcast design, I produced the print layout for the voter guide and the election results, designed and built the Shorthand results page, and created branded social media assets for publishing live results across Twitter and Instagram, ensuring a cohesive visual identity across platforms.
		</p>

	<div class="mb-10 md:mx-50 mx-10">
		<div class="">
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="https://www.youtube.com/watch?v=3R1pDBmqDnY" target="_blank">Broadcast</a></button>
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="https://elonnewsnetwork.shorthandstories.com/election2024/index.html" target="_blank">Election Site</a></button>
		</div>
	</div>

		<section class="max-w-4xl mx-auto">

			<div class="grid md:grid-cols-3 grid-cols-1 mt-4 justify-items-center">

				{#each image as image}

						<Lightbox>
							{#if image.type==="img"}
								<img src={image.src} class="object-cover aspect-16/9 object-top">
							{:else if image.type==="video"}
						<video
							class="object-cover cursor-pointer"
							muted
							loop
							autoplay
							controls
						>
							<source src={image.src} type="video/mp4" />
						</video>
							{/if}
						</Lightbox>
				{/each}

			</div>

			<div class="grid md:grid-cols-3 grid-cols-1 justify-items-center">
				<a href="/img/election/voterguide.pdf" target="_blank">
					<img src="/img/election/voterguide.png" class="mb-2 object-cover object-top " alt=""/>
				</a>
				<a href="/img/election/electionpaper.pdf" target="_blank">
					<img src="/img/election/electionpaperfinal.png" class="mb-2 object-cover object-top " alt=""/>
				</a>
				<a href="https://elonnewsnetwork.shorthandstories.com/election2024/index.html" target="_blank">
					<div class="lg:h-[460px] sm:h-[400px] overflow-y-auto">
					<img
						src="/img/election/webpage.jpg"
						alt="Website Design"
						class="w-full"
					/>
				</div>
				</a>
			</div>



		</section>

	</div>
	<Footer/>
</section>