<script>

	import CheckThisOut from './CheckThisOut.svelte';
	import OtherSections from './OtherSections.svelte';

	export let categories = [
						{
			name: "Graphic Design",
			link: "/graphics",
		},
		{
			name: "Layout Design",
			link: "/layout",
		},
		{
			name: "Motion Design",
			link: "/motion",
		},
		{
			name: "Web Design",
			link: "/web",
		},

	];

</script>

<div class="mx-auto max-w-2xl px-8 py-4 sm:px-6 lg:max-w-6xl">
		<div class="mb-6 grid grid-cols-1 gap-x-6 gap-y-5 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
			{#each categories as cat}
			<div class="group relative">
				<a href={cat.link}>
					<button class="w-full rounded-xl bg-[#457996] text-white font-fredoka uppercase font-semibold text-4xl p-10 h-full object-cover cursor-pointer group-hover:opacity-75 ">{cat.name}</button>
<!--					<img src="{cat.image}" alt="{cat.name}" class="w-full rounded-md bg-gray-200 object-cover group-hover:opacity-75 " />-->
			</a>
<!--				<p class="font-bold text-gray-400 mt-3 md:mb-5 dark:text-white font-inter text-lg text-center">-->

			<!--{cat.name}</p>-->
			</div>
				{/each}
		</div>
	</div>
