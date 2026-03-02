
<script>
	export let experiences = [
		{
			company: "PNY Technologies",
			link: "https://www.pny.com",
			role: "Front-End Web Design Intern",
			dates: "May 2025 - Present",
			description: "Maintain, update and develop web content for PNY sites using HTML5, CSS and JavaScript/jQuery. Assist in the creation of graphics for web design, banner advertising, and social media content.",
		},
		{
			company: "Elon News Network",
			link: "https://www.elonnewsnetwork.com/",
			role: "Design Chief",
			dates: "December 2023 - May 2025",
			description: "Lead and mentor a team of designers, providing guidance on style guidelines and fostering their creative process. Collaborate with Managing Editor of The Pendulum to ensure a clear and concise layout for the weekly paper.",

		},
		{
			company: "Rising Phoenix",
			link: "https://www.elonphoenix.com/sports/rising-phoenix",
			role: "Director of Graphic Design",
			dates: "September 2023 - May 2025",
			description: "Oversee graphic design team to ensure innovative visual storytelling. Design a compelling and consistent brand identify for all Rising Phoenix projects.",
		},
		{
			company: "PNY Technologies",
			link: "https://www.pny.com",
			role: "Front-End Web Design Intern",
			dates: "June 2024 - August 2024",
			description: "Maintain, update and develop web content for PNY sites using HTML5, CSS and JavaScript/jQuery. Assist in the creation of graphics for web design, banner advertising, and social media content.",
		},
		{
			company: "Destination Decoded",
			link: "https://destinationdecoded.com/",
			role: "Jr. Graphic Design Intern",
			dates: "May 2023 - August 2023",
			description: "Collaborated with lead designers and copywriters to create print and digital assets for luxury hospitality brands. Assisted in advancing project management, file sharing, and reporting systems. Performed various daily creative production tasks, including research, mood board creation, and proofreading.",
		}
	];
</script>

<section class="max-w-4xl mx-auto px-6 pt-16">
	<h2 class="font-bold text-[#457996] dark:text-white mb-3 font-fredoka uppercase text-5xl text-center">
		Experience
	</h2>

	<div class="text-center mb-10">
	<button type="button" class="text-gray-400 text-center focus:outline-none hover:text-gray-800 focus:ring-4 focus:ring-gray-100 font-inter font-medium rounded-lg text-sm me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"><a href="img/ErinMartin_Resume.pdf" target="_blank" download><i class="fa fa-download"></i> Download my full resume</a></button>
	</div>

	<div class="space-y-10 mb-15">
		{#each experiences as exp}
			<div class="p-6 bg-white dark:bg-gray-800 rounded-2xl shadow-md">
				<div class="flex justify-between">
				<h3 class="text-2xl font-bold uppercase font-fredoka text-gray-800 dark:text-white">
					{exp.role}
				</h3>
				<p class="text-sm font-inter text-[#457996] dark:text-gray-300 mb-3">
					{exp.dates}
				</p>
				</div>
				<p class="pt-2 text-sm font-inter  uppercase text-[#457996] dark:text-gray-300 mb-3">
					<a href={exp.link} class="hover:underline" target="_blank">{exp.company}</a>
				</p>
				<ul class="font-inter space-y-2 text-gray-400 dark:text-gray-200">
						<li>{exp.description}</li>
				</ul>
			</div>
		{/each}
	</div>
</section>
