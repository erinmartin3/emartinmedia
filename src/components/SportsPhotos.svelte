<script>
	import { Lightbox } from 'svelte-lightbox';

	const photos = [
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-01.jpg" },
		{ src: "/img/sports/trophyup.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-03.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-04.jpg" },
		{ src: "/img/sports/leland.png" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-02.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-05.jpg" },
		{ src: "/img/sports/tennisswing.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-12.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-08.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-09.jpg" },
		{ src: "/img/sports/holi.jfif" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-11.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-25.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-10.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-13.jpg" },
		{ src: "/img/sports/protest.jfif" },
		{ src: "/img/sports/celebrationwbb.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-14.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-06.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-15.jpg" },
		{ src: "/img/sports/clinton.jfif" },
		{ src: "/img/sports/celebration2.jpg" },
		// { src: "/img/sports/erin_martin_ncaa_photoportfolio-16.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-18.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-19.jpg" },
		// { src: "/img/sports/huddle.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-20.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-23.jpg" },
		{ src: "/img/sports/erin_martin_ncaa_photoportfolio-21.jpg" },
		// { src: "/img/sports/erin_martin_ncaa_photoportfolio-22.jpg" },
		// { src: "/img/sports/erin_martin_ncaa_photoportfolio-24.jpg" },
	];

</script>

<div class="flex flex-wrap grid	grid-cols-2 md:grid-cols-4 pb-5">
	{#each photos as photo, i}
		<Lightbox>
			<img src={photo.src} class="object-cover aspect-4/3 object-center"  alt="Erin Martin">
		</Lightbox>
	{/each}
</div>
