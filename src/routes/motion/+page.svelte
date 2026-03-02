<script>
	import Graphics from '../../components/Graphics.svelte';
	import NavBar from '../../components/NavBar.svelte';
	import Footer from '../../components/Footer.svelte';
	import WorkSections from '../../components/WorkSections.svelte';
	import LayoutDesign from '../../components/LayoutDesign.svelte';
	import Nav2 from '../../components/Nav2.svelte';
	import Motion from '../../components/Motion.svelte';
</script>

<div class="bg-gray-100">
	<NavBar/>
	<Nav2 active="motion" />
	<div class="max-w-7xl mx-auto px-10">
		<Motion/>
		<div class="flex justify-center my-5">
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="/work/enntonight" >ENN Motion Graphics</a></button>
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="/work/bea"> BEA Motion Graphics</a></button>
			<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="/work/ennelection"> 2024 Election Graphics</a></button>
		</div>
	</div>
	<Footer/>
</div>