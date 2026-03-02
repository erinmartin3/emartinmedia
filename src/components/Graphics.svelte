<script>
	import { Lightbox } from 'svelte-lightbox';

	const graphics = [
		{ src: "/img/graphics/golf.jpg", name:"RP Graphic" },
		{ src: "/img/graphics/torriihunter.jpg", name:"RP Graphic" },
		{ src: "/img/graphics/caafootballawards.png", name:"RP Graphic" },
		{ src: "/img/graphics/reboundstat.png", name:"RP Graphic" },
		{ src: "/img/graphics/cbiinvite.png", name:"RP Graphic" },
		{ src: "/img/graphics/softballwalkup.png", name:"RP Graphic" },
		{ src: "/img/graphics/blocksrecord.png", name:"RP Graphic" },
		{ src: "/img/graphics/spotifywrapped.png", name:"RP Graphic" },
		{ src: "/img/graphics/springball.png", name:"RP Graphic" },
		{ src: "/img/graphics/yourenext.png", name:"RP Graphic" },
		{ src: "/img/graphics/softballchamp.png", name:"RP Graphic" },
		{ src: "/img/graphics/caachamps.png", name:"RP Graphic" }
	];

</script>

<div class="bg-gray-100">
	<div class="flex flex-wrap grid	grid-cols-2 sm:grid-cols-4 md:grid-cols-5 lg:grid-cols-6 pb-10">
		{#each graphics as graphic, i}
			<Lightbox>
				<img src={graphic.src} class="object-cover aspect-4/5 object-bottom"  alt="{graphic.name}">
			</Lightbox>
		{/each}
	</div>
</div>