<script>
 import { Lightbox } from 'svelte-lightbox';

 const video = [
		{ src: "/img/videos/intro.mp4"},
	 { src: "/img/enntonight/lowerthird.mp4"},

	 { src: "/img/videos/lowerthird.mp4"},
	 { src: "/img/enntonight/ots.mp4"},

	 { src: "/img/videos/looper.mp4" },
	 { src: "/img/election/liveshot1.mp4"},

	 { src: "/img/enntonight/social.mp4"},
	 { src: "/img/election/electionopen2.mp4"},

	 { src: "/img/election/electionpreshow.mp4" },

 ];
</script>

	<div class="grid md:grid-cols-3 grid-cols-1 my-4 justify-items-center">

		{#each video as video}
			<Lightbox>
				<video
					class="object-cover cursor-pointer"
					muted
					loop
					autoplay
				>
					<source src={video.src} type="video/mp4" />
				</video>
			</Lightbox>
		{/each}

	</div>

