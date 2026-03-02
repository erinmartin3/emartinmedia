<script>
	export let active = "";
</script>

<div class="flex flex-wrap gap-4 my-6 justify-center">
	<a
		href="/layout"
		class={`px-5 py-2.5 rounded-lg text-sm font-inter font-medium transition
		${active === "layout"
			? "bg-[#457996] text-white"
			: "bg-gray-800 text-white hover:bg-gray-400 "}`}
	>
		Layout Design
	</a>

	<a
		href="/graphics"
		class={`px-5 py-2.5 rounded-lg text-sm font-inter font-medium transition
		${active === "graphics"
			? "bg-[#457996] text-white"
			: "bg-gray-800 text-white hover:bg-gray-400 "}`}
	>
		Graphic Design
	</a>

	<a
		href="/motion"
		class={`px-5 py-2.5 rounded-lg text-sm font-inter font-medium transition
		${active === "motion"
			? "bg-[#457996] text-white"
			: "bg-gray-800 text-white hover:bg-gray-400 "}`}
	>
		Motion Design
	</a>

	<a
		href="/web"
		class={`px-5 py-2.5 rounded-lg text-sm font-inter font-medium transition
		${active === "web"
			? "bg-[#457996] text-white"
			: "bg-gray-800 text-white hover:bg-gray-400 "}`}
	>
		Web Design
	</a>
</div>