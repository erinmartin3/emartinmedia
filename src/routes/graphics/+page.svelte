<script>
	import Graphics from '../../components/Graphics.svelte';
	import NavBar from '../../components/NavBar.svelte';
	import Footer from '../../components/Footer.svelte';
	import WorkSections from '../../components/WorkSections.svelte';
	import Nav2 from '../../components/Nav2.svelte';
</script>

<div class="bg-gray-100">
<NavBar/>
	<Nav2 active="graphics" />
	<Graphics/>
<Footer/>
</div>