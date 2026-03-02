<script>
	let filter = "all";

	const projects = [
		{
			title: "ENN Election 2024",
			image: "/img/election.png",
			type: "img",
			link2:"https://elonnewsnetwork.shorthandstories.com/elon-news-network-election-center-2025/index.html",
			link:"/work/ennelection",

		},
		{
			title: "Rocket League",
			image: "/img/EsportsDomMedia.jpg",
			type: "img",
			link2:"https://elonnewsnetwork.shorthandstories.com/elonesports/index.html",
			link:"/work/rocketleague",
		},
		{
			title: "MixFolio",
			image: "/img/mixfolio.jpg",
			description: "Personal Project",
			type: "img",
			link2:"https://mixfolio.vercel.app",
			link:"/work/mixfolio",
		},
	];

</script>

<section class="bg-gray-100">

	<section class="max-w-4xl mx-auto px-6 pb-16">

		<div class="flex grid grid-cols-1 md:grid-cols-3 justify-items-center gap-6 cursor-pointer">
			{#each projects as project (project.title)}
						<div class="flex-1 min-w-[250px] max-w-sm bg-white p-4 rounded-xl shadow hover:-translate-y-1 transition-transform">
							<a href={project.link}>

							{#if project.type==="img"}
								<img src={project.image} class="aspect-16/9 object-cover object-top rounded-md mb-3" alt={project.title} />
							{/if}
							<div class="flex justify-between">
								<h3 class="font-bold font-inter text-lg mb-2">{project.title}</h3>
								<p class="mt-2 inline-block text-xs px-2 rounded font-inter text-gray-500">{project.description}</p>
							</div>
					</a>
							<a href={project.link2}>
		<span class="mr-1 my-1 inline-block text-xs px-2 py-1 rounded font-inter bg-[#457996]  text-white hover:bg-gray-400">
		Live Site
		</span></a>
								<a href={project.link}><span class="mr-1 my-1 inline-block text-xs px-2 py-1 rounded font-inter bg-gray-800  text-gray-500 text-white hover:bg-gray-400">
		Project Details
	</span></a>
						</div>
			{/each}
		</div>

	</section>
</section>