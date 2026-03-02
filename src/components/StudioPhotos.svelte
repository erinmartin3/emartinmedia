<script>
	import { Lightbox } from 'svelte-lightbox';

	const photo3 = [
		{ src: "/img/studio/studio1.jpg" },
		{ src: "/img/studio/studio2.jpg" },
		{ src: "/img/studio/studio3.jpg" },
		{ src: "/img/studio/studio4.jpg" },
		{ src: "/img/studio/studio5.jpg" },
		{ src: "/img/studio/studio6.jpg" },
		{ src: "/img/studio/studio7.jpg" },
		{ src: "/img/studio/studio8.jpg" },
	];

</script>


<!--<div class="flex flex-wrap grid	grid-cols-3 md:grid-cols-5">-->
<!--	{#each photo2 as photos, i}-->
<!--		<Lightbox>-->
<!--			<img src={photos.src} class="object-cover aspect-3/4 object-center"  alt="Erin Martin">-->
<!--		</Lightbox>-->
<!--	{/each}-->
<!--	<img src="/img/studio/finest5.jpg" class="object-cover aspect-3/4 object-center md:hidden"  alt="Erin Martin">-->

<!--</div>-->

<!--<img src="/img/studio/bball3.jpg" class="w-full" />-->


<!--<div class="flex flex-wrap grid	grid-cols-3 md:grid-cols-5">-->
<!--	{#each photos as photo, i}-->
<!--		<Lightbox>-->
<!--			<img src={photo.src} class="object-cover aspect-3/4 object-center"  alt="Erin Martin">-->
<!--		</Lightbox>-->
<!--	{/each}-->
<!--	<img src="/img/studio/bball2.jpg" class="object-cover aspect-3/4 object-center md:hidden"  alt="Erin Martin">-->
<!--</div>-->



<div class="flex flex-wrap grid	grid-cols-2 md:grid-cols-4 pb-5">
	{#each photo3 as photo, i}
		<Lightbox>
			<img src={photo.src} class="object-cover aspect-square object-top"  alt="Erin Martin">
		</Lightbox>
	{/each}
</div>

