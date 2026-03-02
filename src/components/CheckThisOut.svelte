<script>

	export let examples = [
		{
			name: "Motion Design",
			link: "https://destinationdecoded.com/",
		},
		{
			name: "Layout Design",
			link: "https://destinationdecoded.com/",
		},
		{
			name: "Photography",
			link: "https://destinationdecoded.com/",
		}
	];

</script>

<p class="mb-5 lg:mb-5 font-inter font-medium text-center text-gray-500 dark:text-gray-400 sm:text-xl">Some of my recent work...</p>

<section class="flex justify-center mb-17">

<div class="flex items-center gap-8">
	{#each examples as exp}
			<button type="button" class="text-white bg-[#457996] border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href={exp.link}>{exp.name}</a></button>
		{/each}
</div>
</section>