<script>
	import { onMount } from "svelte";

	const professions = ["Designer", "Developer", "Creative", "Storyteller"];
	let index = 0;
	let animatedText = "";
	let isDeleting = false;

	function typeLoop() {
		const currentProfession = professions[index];
		const speed = isDeleting ? 50 : 100;

		if (isDeleting) {
			animatedText = currentProfession.substring(0, animatedText.length - 1);
		} else {
			animatedText = currentProfession.substring(0, animatedText.length + 1);
		}

		if (!isDeleting && animatedText === currentProfession) {
			setTimeout(() => {
				isDeleting = true;
				typeLoop();
			}, 2000);
			return;
		} else if (isDeleting && animatedText === "") {

			isDeleting = false;
			index = (index + 1) % professions.length;
			setTimeout(typeLoop, 500);
			return;
		}

		setTimeout(typeLoop, speed);
	}

	onMount(() => {
		typeLoop();
	});
</script>

<header>
	<h1 class="text-4xl font-bold font-fredoka tracking-wide text-gray-800">
		My name is Erin Martin,<br>
		I'm a{" "}
		<span
			class="inline-block whitespace-nowrap text-[#457996] border-r-2 animate-blink-caret"
		>
      {animatedText}
    </span>
	</h1>
</header>

<style>
    @keyframes blink-caret {
        from,
        to {
            border-color: transparent;
        }
        50% {
            border-color: gray;
        }
    }

    .animate-blink-caret {
        animation: blink-caret 0.75s step-end infinite;
    }
</style>
