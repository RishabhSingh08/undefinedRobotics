<script>
	import '../app.css';
	import Navbar from '../lib/components/Navbar.svelte';
	import Footer from '../lib/components/Footer.svelte';

	let { children } = $props();
</script>

<style>
	.dm-sans {
		font-family: "DM Sans", sans-serif;
		font-optical-sizing: auto;
		font-weight: 400;
		font-style: normal;
	}
</style>

<main class="bg-gradient-to-b from-black to-gray-900 text-white dm-sans ">
	<Navbar />
		{@render children()}
	<Footer />
</main>
