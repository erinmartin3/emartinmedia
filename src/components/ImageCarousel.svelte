<script>
	import { onMount } from "svelte";

	let current = 0;
	const interval = 8000;

	const slides = [
		{ src: "/img/story/photostory_hearstentry-1.jpg", description:"Delegates and guests hold up \"We <3 Joe\" signs in the United Center as President Joe Biden speaks at the Democratic National Convention on Aug. 19, 2024."},
		{ src: "/img/story/photostory_hearstentry-2.jpg", description:"Minnesota Gov. Tim Walz fist bumps a delegate at the first night of the Democratic National Convention on Aug. 19, 2024."},
		{ src: "/img/story/photostory_hearstentry-3.jpg", description:"Former Vice President Kamala Harris steps onstage at the Democratic National Convention in Chicago on Aug. 19, 2024 to welcome delegates and visitors to the convention."},
		{ src: "/img/story/photostory_hearstentry-4.jpg", description:"A delegate at the Democratic National Convention holds a “We Fight, We Win.” sign on the first night of the Democratic National Convention on Aug. 19, 2024."},
		{ src: "/img/story/photostory_hearstentry-5.jpg", description:"Former President Barack Obama speaks at the Democratic National Convention on Aug. 20, 2024. Obama endorsed former Vice President Kamala Harris and took a jab at former President Donald Trump, saying, \"We do not need four more years of bluster and bumbling and chaos. We have seen that movie before, and we all know that the sequel is usually worse.\""},
		{ src: "/img/story/photostory_hearstentry-6.jpg", description:"Delegates and guests hold up American flags and “USA” posters at the final night of the Democratic National Convention on Aug. 22, 2024."},
		{ src: "/img/story/photostory_hearstentry-7.jpg", description:"Former Vice President Kamala Harris smiles onstage in front of nearly 25,000 delegates and guests in the United Center prior to accepting the Democratic Party's Presidential nomination."},
		{ src: "/img/story/photostory_hearstentry-8.jpg", description:"An attendee takes a photo of former Vice President Kamala Harris delivering her official speech accepting the Democratic party’s presidential nominee Aug. 22, 2024 at the DNC. Harris’ acceptance speech attracted 28.9 million viewers, which edged out former President Donald Trump’s speech in Milwaukee at the Republican National Convention in July, which was watched by 28.4 million viewers. According to Nielsen data, the DNC attracted an average of 21.8 million viewers."},
		{ src: "/img/story/photostory_hearstentry-9.jpg", description:"Balloons and confetti fill Chicago's United Center as the 2024 Democratic National Convention concludes its fourth and final night, marking former Vice President Kamala Harris’s historic moment as the first Black woman and first Asian American to accept a major party's presidential nomination."},
		{ src: "/img/story/photostory_hearstentry-10.jpg", description:"Former Vice President Kamala Harris and former Second Gentleman Doug Emhoff wave goodbye to the crowd as they exit the stage at the Democratic National Convention on Aug. 22, 2024."}
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
		At DNC, Democrats highlight <br> stakes of November Election
	</h2>

	<div class="relative h-60 md:h-80 overflow-hidden">
		{#each slides as slide, i}
			<img
				src={slide.src}
				alt={slide.description}
				class="absolute inset-0 w-full h-full object-contain transition-opacity duration-700 ease-in-out
          {i === current ? 'opacity-100' : 'opacity-0'}"
			/>
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

	<p class="text-center text-xs text-bold text-inter text-gray-400 mb-5 mx-10">The above photo story was awarded top 20 in the Hearst Photojournalism Picture Story/Series Competition as a part of the 2025 Hearst Journalism Awards Program.</p>
