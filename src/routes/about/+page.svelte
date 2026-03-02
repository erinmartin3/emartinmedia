<script>
	import Footer from '../../components/Footer.svelte';
	import NavBar from '../../components/NavBar.svelte';
	import Hero from '../../components/Hero.svelte';
	import ImageCarousel from '../../components/ImageCarousel.svelte';
	import Images from '../../components/Images.svelte';
	import CheckThisOut from '../../components/CheckThisOut.svelte';
	import AnimatedHeader from '../../components/AnimatedHeader.svelte';
	import Awards from '../../components/Awards.svelte';

	let award="pt-10";
</script>

<NavBar/>

<footer class="px-8 bg-gray-100">
	<div class="container mx-auto">
		<div
			class="flex flex-wrap items-center gap-y-4 border-t text-gray-400 border-gray-300 py-6 justify-between">

	<div class="max-w-7xl mx-auto">
	<div class="grid md:grid-cols-5 gap-4 items-start">
		<div class="md:col-span-2 flex justify-center lg:mb-10 mt-5 mb-0">
				<Images/>
					</div>
		<div class="md:col-span-3 lg:ml-5 mb-10">
			<h2 class="font-bold text-[#457996] dark:text-white mb-6 mt-5 font-fredoka uppercase text-4xl">About</h2>
			<div class="flex items-center">
				<ol class="grid grid-cols-1 gap-4 content-center font-inter font-regular text-gray-800 md:text-md dark:text-gray-400">
					<li>I am a multidisciplinary visual storyteller based in Washington, DC. I bring extensive internship, freelance and student media experience, along with a background in computer science and communications. I aim to create meaningful digital work that blends creativity and technology.</li>
				</ol>
			</div>
			<h2 class="font-bold text-[#457996] dark:text-white mb-6 mt-10 font-fredoka uppercase text-4xl">Software</h2>
			<div class="flex items-center">
				<ol class="grid grid-cols-1 gap-4 content-center font-inter font-regular text-gray-800 md:text-md dark:text-gray-400">
					<li><b>Graphic Design:</b> Adobe InDesign, Adobe Illustrator, Adobe Photoshop</li>
					<li><b>Motion Design:</b> Adobe After Effects, Adobe Premiere Pro, Blender</li>
					<li><b>Web Development:</b> Figma, Adobe XD, HTML, CSS, JavaScript, Svelte, React.js, Node.js, Tailwind, WordPress</li>
				</ol>
			</div>
			<Awards/>
			<div class="mt-8">
			<button type="button" class="text-white bg-[#457996] border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="/layout">Explore My Work</a></button>
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="mailto:erinmartin612@gmail.com">Let's Chat</a></button>
			</div>
		</div>
		</div>
			</div>

		</div>
		</div>
</footer>

<Footer/>
