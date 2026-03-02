<script>
	import { onMount } from "svelte";

	let current = 0;
	const interval = 8000;

	const slides = [
		{ src: "/img/story2/edited_photostory_40.jpg", description:"As the name suggests, the 7 a.m. Tailgate Crew at Elon University begins tailgating at 7 o'clock before each Elon football home game. "},
		{ src: "/img/story2/edited_photostory_10.jpg", description:"The crew is comprised of alumni Brian Martindale '95, David Rich '87, football alumnus David Oakley '91 and Burlington resident Mike Cross."},
		{ src: "/img/story2/edited_photostory_15.jpg", description:"Prior to each home game, the crew proudly hoists their custom \"7 a.m. Tailgate Crew\" flag into the air, and broadcasts their message on their Twitter account, @Elon7amTailgate, which boasts over 1,000 followers."},
		{ src: "/img/story2/edited_photostory_5.jpg", description:"Over the years, each member has assumed a specific responsibility. Martindale manages social media, ensuring frequent updates on Twitter. Rich oversees drinks and bartending needs. Cross focuses on setting up live TV to keep the group informed about other soccer or football games. Lastly, Oakley takes charge of the grill, ensuring the main course is ready to go."},

		{ src: "/img/story2/edited_photostory_25.jpg", description:"The culinary offerings at their tailgates are diverse, ranging from pulled pork and chicken wings to seafood, breakfast dishes, and the Homecoming classic—a full pig."},
		{ src: "/img/story2/edited_photostory_7.jpg", description:"Their tailgate has evolved into an integral part of Elon's tailgate culture, attracting various members of the Athletic Department and the university community. "},
		{ src: "/img/story2/edited_photostory_21.jpg", description:"Beyond the essential elements of good food and drinks, the day unfolds with games like cornhole, fostering a lively atmosphere."},
		{ src: "/img/story2/edited_photostory_20.jpg", description:"Digging deeper, the crew's support for Elon extends beyond the tailgate. All four members—Martindale, Oakley, Rich, and Cross—are part of the Phoenix Club’s Athletic Advisory Board and significant donors to the athletic department."},
		{ src: "/img/story2/edited_photostory_29.jpg", description:"Rich expressed his appreciation for the tailgate's ability to foster connections with students, staff, and the broader Elon sports community."},
		{ src: "/img/story2/edited_photostory_3.jpg", description:"While the core four always provide the main course, the tailgate receives support from friends and other attendees who contribute sides and desserts to complete the culinary experience."},

	];

	function next() {
		current = (current + 1) % slides.length;
	}

	function prev() {
		current = (current - 1 + slides.length) % slides.length;
	}

	function goTo(i) {
		current = i;
	}

	onMount(() => {
		const timer = setInterval(next, interval);
		return () => clearInterval(timer);
	});
</script>


<div class="relative w-full">

	<h2 class="font-bold text-[#457996] dark:text-white font-fredoka text-3xl text-center mx-10 mb-4">
		The story of the <br> 7 AM tailgate crew
	</h2>

	<div class="relative h-60 md:h-80 overflow-hidden">
		{#each slides as slide, i}
			<img
				src={slide.src}
				alt={slide.description}
				class="absolute inset-0 w-full h-full object-contain transition-opacity duration-700 ease-in-out
          {i === current ? 'opacity-100' : 'opacity-0'}"
			/>
<!--			<div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-gray-800/100 to-transparent p-12 {i === current ? 'opacity-100' : 'opacity-0'}">-->
<!--				<p class="text-center text-xs text-bold text-inter text-shadow-lg  text-gray-200">{slide.description}</p>-->
<!--			</div>-->
		{/each}
	</div>



	<!-- Indicators -->
	<div class="absolute bottom-5 left-1/2 -translate-x-1/2 z-20 flex space-x-3">
		{#each slides as _, i}
			<button
				class="w-3 h-3 rounded-full {i === current ? 'bg-white' : 'bg-gray-400/50'}"
				on:click={() => goTo(i)}
				aria-label="Go to slide {i + 1}"
			></button>
		{/each}
	</div>

<!--	&lt;!&ndash; Controls &ndash;&gt;-->
<!--	<button-->
<!--		class="absolute top-0 left-0 z-20 flex items-center justify-center h-full px-4 group focus:outline-none"-->
<!--		on:click={prev}-->
<!--	>-->
<!--    <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-gray-700/50 group-hover:bg-gray-700/20">-->
<!--      <svg class="w-5 h-5 text-white" fill="none" viewBox="0 0 6 10" stroke="currentColor">-->
<!--        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 1 1 5l4 4"/>-->
<!--      </svg>-->
<!--    </span>-->
<!--	</button>-->

<!--	<button-->
<!--		class="absolute top-0 right-0 z-20 flex items-center justify-center h-full px-4 group focus:outline-none"-->
<!--		on:click={next}-->
<!--	>-->
<!--    <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-gray-700/50 group-hover:bg-gray-700/20">-->
<!--      <svg class="w-5 h-5 text-white" fill="none" viewBox="0 0 6 10" stroke="currentColor">-->
<!--        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 9l4-4-4-4"/>-->
<!--      </svg>-->
<!--    </span>-->
<!--	</button>-->

</div>

<div class="text-center">
	<p class="p-5 pb-4 font-inter text-sm font-medium text-gray-700 dark:text-gray-300 max-w-xl mx-auto">
		{slides[current].description}
	</p>
</div>