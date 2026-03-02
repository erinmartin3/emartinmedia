<script>
	let filter = "Design";

	const projects = [
		{
			title: "ENN Tonight Graphics",
			image: "/img/enntonight.png",
			category: ["Motion","Design"],
			type: "img",
			link:"/work/enntonight",
		},
		{
			title: "ENN Election 2024",
			image: "/img/election.png",
			category: ["Motion","Design", "Logo"],
			type: "img",
			link:"/work/ennelection",
		},
		{
			title: "Rocket League",
			image: "/img/EsportsDomMedia.jpg",
			category: ["Design", "Data", "Reporting"],
			type: "img",
			link:"/work/rocketleague",
		},
		// {
		// 	title: "Revolving Door",
		// 	image: "/img/revolvingdoor.png",
		// 	category: ["Design", "Data"],
		// 	type: "img",
		// 	link:"",
		// },
		{
			title: "MixFolio",
			image: "/img/mixfolio.jpg",
			category: ["Design", "Development"],
			description: "Personal Project",
			type: "img",
			link:"/work/mixfolio",
		},
		{
			title: "BEA Awards Show",
			image: "/img/bea2.png",
			category: ["Motion", "Design"],
			type: "img",
			link:"/work/bea",
		},
	];

	function setFilter(category) {
		filter = category;
	}

	function isVisible(project) {
		return filter === "all" || project.category.includes(filter);
	}
</script>

<section class="bg-gray-100">

	<h2 class="font-bold text-[#457996] mb-10 md:mb-5 mb-4 dark:text-white font-fredoka uppercase md:text-5xl text-4xl text-center">
		Featured Projects
	</h2>

	<section class="max-w-4xl mx-auto pb-16">
<!--<Breadcrumbs webpage={"Test3"} category={"Graphic Design"} link={"/graphicdesign"}/>-->

		<div class="flex flex-wrap gap-4 mb-6 justify-center">
<!--			<button-->
<!--				on:click={() => setFilter("all")}-->
<!--				class="px-4 font-inter py-2 rounded-lg transition-colors"-->
<!--				class:selected={filter === "all"}-->
<!--				class:bg-gray-800={filter === "all"}-->
<!--				class:text-white={filter === "all"}-->
<!--				class:bg-gray-200={filter !== "all"}-->
<!--			>-->
<!--				All-->
<!--			</button>-->

			<button
				on:click={() => setFilter("Design")}
				class="px-4 py-2 font-inter rounded-lg transition-colors"
				class:bg-gray-800={filter === "Design"}
				class:text-white={filter === "Design"}
				class:bg-gray-200={filter !== "Design"}
			>
				Design
			</button>


			<button
				on:click={() => setFilter("Development")}
				class="px-4 py-2 font-inter rounded-lg transition-colors"
				class:bg-gray-800={filter === "Development"}
				class:text-white={filter === "Development"}
				class:bg-gray-200={filter !== "Development"}
			>
				Development
			</button>

			<button
				on:click={() => setFilter("Motion")}
				class="px-4 py-2 font-inter rounded-lg transition-colors"
				class:bg-gray-800={filter === "Motion"}
				class:text-white={filter === "Motion"}
				class:bg-gray-200={filter !== "Motion"}
			>
				Motion Graphics
			</button>
		</div>

		<div class="flex grid grid-cols-1 md:grid-cols-3 justify-items-center gap-6 cursor-pointer">
			{#each projects as project (project.title)}
				{#if isVisible(project)}
					<a href={project.link}>
					<div class="flex-1 min-w-[250px] max-w-sm bg-white dark:bg-gray-900 p-4 rounded-xl shadow hover:-translate-y-1 transition-transform">
						{#if project.type==="img"}
						<img src={project.image} class="aspect-16/9 object-cover object-top rounded-md mb-3" alt={project.title} />
							{:else if project.type=="video"}
							<video
								class="object-cover  aspect-16/9 object-cover object-top rounded-md mb-3"
								muted
								autoplay
								loop
							>
								<source src={project.image} type="video/mp4" />
							</video>
						{/if}
							<div class="flex justify-between">
						<h3 class="font-bold font-inter text-lg mb-2">{project.title}</h3>
							<p class="mt-2 inline-block text-xs px-2 rounded font-inter text-gray-500">{project.description}</p>
						</div>
						{#each project.category as cat}
	<span class="mr-2 my-1 inline-block text-xs px-2 py-1 rounded font-inter bg-gray-100 dark:bg-gray-700 text-gray-500">
		{cat}
	</span>
						{/each}
					</div>
					</a>
				{/if}
			{/each}
		</div>

	</section>
</section>