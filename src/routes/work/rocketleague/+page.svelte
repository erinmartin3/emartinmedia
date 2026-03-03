<script>
import Footer from '../../../components/Footer.svelte';
import NavBar from '../../../components/NavBar.svelte';
import { Gallery, Video } from 'flowbite-svelte';

</script>

<section class="bg-gray-100">

	<NavBar/>

	<div class=" max-w-7xl mx-auto mt-6">
		<div class="flex justify-center">
			<h2 class="font-bold text-[#457996] my-5 md:mb-7 mb-4  font-fredoka uppercase md:text-5xl text-4xl text-center">
				Rocket League	Sparks Connection
			</h2>
		</div>
		<div class="mb-10 md:mx-50 mx-10">
			<p class="">
				I independently led every aspect of this project — reporting, writing, photographing, filming, designing the layout and creating original data visualizations. From concept to publication, I managed the full production process to deliver a cohesive and visually engaging feature across print, web and video formats.
				<br><br>
			</p>

			<div class="">
				<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 "><a href="/img/rocketleague.pdf" target="_blank">Print</a></button>
				<button type="button" class="text-white bg-gray-800 border border-gray-300 focus:outline-none hover:bg-gray-400 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 "><a href="https://elonnewsnetwork.shorthandstories.com/elonesports/index.html" target="_blank">Digital Story</a></button>

			</div>

			<div class="grid md:grid-cols-2 grid-cols-1 gap-4 my-5 ">
				<div>
					<a href="/img/rocketleague.pdf" target="_blank">
						<img src="/img/rocketleague2.png" class="mb-2 object-cover object-top " alt=""/>
					</a>
				</div>
				<div>
					<a href="https://elonnewsnetwork.shorthandstories.com/elonesports/index.html" target="_blank">
						<Video src="/img/videos/rocketleague.mp4" autoplay muted loop controls trackSrc="rocketleauge.mp4"/>
					</a>
					<div class="h-[300px] overflow-y-auto mt-5">
						<a href="https://elonnewsnetwork.shorthandstories.com/elonesports/index.html" target="_blank"><img
							src="/img/rocketleaugesite.jpg"
							alt="Website Design"
							class="w-full"
						/></a>
					</div>
				</div>
			</div>

		</div>

	<Footer/>
	</div>
</section>