<script>
	import Footer from '../../../components/Footer.svelte';
	import NavBar from '../../../components/NavBar.svelte';
	import { Video } from 'flowbite-svelte';
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
				This personal project was built in collaboration with <a href="https://jakebogan.com" class="hover:underline" target="_blank">Jake Bogan</a> as a streamlined portfolio builder designed for users who need a custom site in minutes.
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

			<a href="/img/barbiecover.pdf" target="_blank" >
				<img class="object-cover object-center w-full rounded-xl hover:-translate-y-1 max-w-full hover:shadow-md"
						 src="/img/womenshistory.jpg"
						 alt="gallery-photo" />
			</a>

		</div>
	</section>
	<Footer/>
</section>