<script>
	import Footer from '../../components/Footer.svelte';
	import NavBar from '../../components/NavBar.svelte';
	import LayoutDesign from '../../components/LayoutDesign.svelte';
	import Reporting from '../../components/Reporting.svelte';
	import Illustrations from '../../components/Illustrations.svelte';
	import DataViz from '../../components/DataViz.svelte';
	import Broadcast from '../../components/Broadcast.svelte';
	import Graphics from '../../components/Graphics.svelte';

	let filter = "Layout";

	function setFilter(category) {
		filter = category;
	}

	function isVisible(project) {
		return filter === "Layout" || project.category === filter;
	}

</script>

<section class="bg-gray-100">

	<NavBar/>

	<div class=" max-w-7xl mx-auto mb-10">
	<div class="flex justify-center">
		<a href="https://www.elonnewsnetwork.com/" target="_blank">
	<img src="/img/clients/ennlogo.png" alt="ENN" class="max-h-50 aspect-video opacity-100 hover:opacity-50 object-contain"/>
		</a>
	</div>
	<p class="mb-5 md:mx-50 mx-10">As Elon News Network's Design Chief I led and mentored a team of 8 designers, providing guidance and fostering their creative process. In my role I collaborated with staff to ensure a clear and concise layout for the weekly paper.
		<br><br>I also led a full redesign and implementation of the broadcast graphics system, partnering with a designer to develop updated visual assets and integrating the complete graphics package into the ROSS production system to support live and recorded broadcasts.
<br><br>Additionally, I worked as a broadcast production member and <a href="https://vimeo.com/erinmartin" class="underline" target="_blank">directed live broadcasts</a> from 2022 to 2025.
	</p>
			<section class="max-w-4xl mx-auto px-6 py-8">
				<!--<Breadcrumbs webpage={"Test3"} category={"Graphic Design"} link={"/graphicdesign"}/>-->

				<div class="flex flex-wrap gap-4 justify-center">

					<button
						on:click={() => setFilter("Layout")}
						class="px-4 py-2 font-inter rounded-lg transition-colors"
						class:bg-gray-800={filter === "Layout"}
						class:text-white={filter === "Layout"}
						class:bg-gray-200={filter !== "Layout"}
					>
						Layout Design
					</button>

					<button
						on:click={() => setFilter("Illustrations")}
						class="px-4 py-2 font-inter rounded-lg transition-colors"
						class:bg-gray-800={filter === "Illustrations"}
						class:text-white={filter === "Illustrations"}
						class:bg-gray-200={filter !== "Illustrations"}
					>
						Editorial Illustrations
					</button>

					<button
						on:click={() => setFilter("Data")}
						class="px-4 py-2 font-inter rounded-lg transition-colors"
						class:bg-gray-800={filter === "Data"}
						class:text-white={filter === "Data"}
						class:bg-gray-200={filter !== "Data"}
					>
						Data Viz
					</button>

					<button
						on:click={() => setFilter("Reporting")}
						class="px-4 py-2 font-inter rounded-lg transition-colors"
						class:bg-gray-800={filter === "Reporting"}
						class:text-white={filter === "Reporting"}
						class:bg-gray-200={filter !== "Reporting"}
					>
						Reporting
					</button>

				</div>

			</section>
			<div class="flex flex-wrap gap-4 lg:px-40 px-5 justify-center">

				<div class="max-w">

					{#if filter === "Layout"}
						<LayoutDesign/>
					{/if}

					{#if filter === "Data"}
						<DataViz/>
					{/if}

					{#if filter === "Illustrations"}
						<Illustrations/>
					{/if}

					{#if filter === "Reporting"}
						<Reporting/>
					{/if}

					<!--{#if filter === "Stories"}-->
					<!--	<PhotoStory/>-->
					<!--{/if}-->

				</div>
			</div>
		</div>
	<Footer/>
</section>