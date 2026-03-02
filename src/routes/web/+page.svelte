<script>
	import NavBar from '../../components/NavBar.svelte';
	import Footer from '../../components/Footer.svelte';
	import Nav2 from '../../components/Nav2.svelte';
	import WebDesign from '../../components/WebDesign.svelte';
</script>

<div class="bg-gray-100">
	<NavBar/>
	<Nav2 active="web" />
	<div class="max-w-7xl mx-auto px-10">
		<WebDesign/>
	</div>
	<Footer/>
</div>