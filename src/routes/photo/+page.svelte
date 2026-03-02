<!--<script>-->
<!--	import Footer from '../../components/Footer.svelte';-->
<!--	import NavBar from '../../components/NavBar.svelte';-->
<!--	import Breadcrumbs from '../../components/Breadcrumbs.svelte';-->
<!--	import ImageCarousel from '../../components/ImageCarousel.svelte';-->
<!--	import Work from '../../components/Work.svelte';-->

<!--</script>-->

<!--<section class="bg-gray-100">-->

<!--<NavBar/>-->

<!--	<div class="bg-gray-800">-->
<!--		<ImageCarousel/>-->
<!--	</div>-->

<!--	<section class="max-w-4xl mx-auto px-6 py-16 text-center">-->
<!--&lt;!&ndash;<Breadcrumbs webpage={"MixFolio"} category={"Web Development"} link={"/work"}/>&ndash;&gt;-->
<!--		<h2 class="font-bold text-[#457996] dark:text-white mb-6 font-fredoka uppercase text-5xl ">-->
<!--Photography-->
<!--		</h2>-->
<!--		<p class="my-5 font-inter font-medium text-gray-800 md:text-lg dark:text-gray-400">Freelance photographer with 4+ years experience in shooting news, sports and portraits.</p>-->

<!--		<div class="mt-10">-->
<!--		<Work/>-->
<!--		</div>-->

<!--		<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="mailto:erinmartin612@gmail.com">Let's Chat</a></button>-->

<!--	</section>-->


<!--	<Footer/>-->
<!--</section>-->

<script>
	import Footer from '../../components/Footer.svelte';
	import NavBar from '../../components/NavBar.svelte';
	import SportsPhotos from '../../components/SportsPhotos.svelte';
	import StudioPhotos from '../../components/StudioPhotos.svelte';
	import PhotoStory from '../../components/PhotoStory.svelte';

	let filter = "Singles";

	function setFilter(category) {
		filter = category;
	}

	function isVisible(project) {
		return filter === "Singles" || project.category === filter;
	}

</script>

<NavBar/>

<div class="bg-gray-100">

<section class="max-w-4xl mx-auto px-6 py-8">
	<!--<Breadcrumbs webpage={"Test3"} category={"Graphic Design"} link={"/graphicdesign"}/>-->

	<div class="flex flex-wrap gap-4 justify-center">

		<button
			on:click={() => setFilter("Singles")}
			class="px-4 py-2 font-inter rounded-lg transition-colors"
			class:bg-gray-800={filter === "Singles"}
			class:text-white={filter === "Singles"}
			class:bg-gray-200={filter !== "Singles"}
		>
			Singles
		</button>

		<button
			on:click={() => setFilter("Portrait")}
			class="px-4 py-2 font-inter rounded-lg transition-colors"
			class:bg-gray-800={filter === "Portrait"}
			class:text-white={filter === "Portrait"}
			class:bg-gray-200={filter !== "Portrait"}
		>
			Portraits
		</button>

<!--			<button-->
<!--			on:click={() => setFilter("Stories")}-->
<!--			class="px-4 py-2 font-inter rounded-lg transition-colors"-->
<!--			class:bg-gray-800={filter === "Stories"}-->
<!--			class:text-white={filter === "Stories"}-->
<!--			class:bg-gray-200={filter !== "Stories"}-->
<!--		>-->
<!--			Stories-->
<!--		</button>-->

	</div>

</section>
	<div class="flex flex-wrap gap-4 justify-center">

		<div class="max-w">

			{#if filter === "Singles"}
				<SportsPhotos/>
			{/if}

			{#if filter === "Portrait"}
				<StudioPhotos/>
			{/if}

			<!--{#if filter === "Stories"}-->
			<!--	<PhotoStory/>-->
			<!--{/if}-->

		</div>
	</div>
<Footer/>
</div>
