<script>

	export let stories = [
		{
			title: "Rocket League sparks connection at Elon",
			link: "https://elonnewsnetwork.shorthandstories.com/elonesports/index.html",
			image: "img/EsportsDomMedia.jpg",
			date: "May 6, 2025",
			role: "🏆 3rd Place, Multimedia Sports Story, ACP",
		},
		{
			title: "Split ticket voting increases across the country",
			link: "https://www.elonnewsnetwork.com/article/2024/11/split-ticket-voting-increases-across-country",
			image: "img/votingimage.jfif",
			date: "November 22, 2024",
		},
		{
			title: "North Carolina Democrats gear up for Election Day",
			link: "https://www.elonnewsnetwork.com/article/2024/08/north-carolina-democrats-gear-up-for-election-day",
			image: "img/ncvoter.jpg",
			date: "August 21, 2024",
		},
		{
			title: "Under the stars: Elon University’s Black Student Union hosts first annual met gala",
			link: "https://www.elonnewsnetwork.com/article/2024/04/elon-university-black-student-union-met-gala",
			image: "img/bsumetgala.jpg",
			date: "April 16, 2024",
		}]
		// ,
		// {
		// 	title: "Elon University expands academic opportunities at Charlotte Regional Center",
		// 	link: "https://www.elonnewsnetwork.com/article/2023/09/elon-university-expands-academic-opportunities-at-charlotte-regional-center",
		// 	image: "img/charlotte.jpg",
		// 	date: "September 19, 2023",
		// }]

</script>

<div class="grid lg:grid-cols-4 grid-cols-2 gap-4">
	{#each stories as story}
		<a href={story.link} target="_blank">
		<div class="p-5 bg-white dark:bg-gray-800 rounded-2xl shadow-md flex flex-wrap hover:-translate-y-1  items-center">
					<img src={story.image} class="sm:rounded-xl rounded-2xl mb-2 object-cover object-center aspect-5/3" alt={story.title} />
			<div class="">
			<h3 class="sm:pt-0 pt-4 text-lg font-bold font-inter font-medium leading-snug hover:underline text-gray-800 dark:text-white">{story.title}</h3>
					<p class="text-sm font-inter font-medium italic mt-1 text-gray-500 dark:text-gray-300">
					{story.date}</p>
				{#if story.role}
					<span
						class="mt-3 inline-block text-xs px-2 py-1 rounded font-inter bg-gray-300 dark:bg-gray-700 text-gray-600"> {story.role}</span>
				{/if}
					</div>
		</div>
		</a>
	{/each}
</div>