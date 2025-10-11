<script>
	import '../app.css';
	import Navbar from '../lib/components/Navbar.svelte';
	import Footer from '../lib/components/Footer.svelte';
import { injectAnalytics } from '@vercel/analytics/sveltekit'
injectAnalytics();
	let { children } = $props();
</script>

<style>
	.dm-sans {
		font-family: "DM Sans", sans-serif;
		font-optical-sizing: auto;
		font-weight: 400;
		font-style: normal;
	}
	/* Offset for fixed navbar height (64px). Adjust if Navbar height changes. */
	.app-content {
		/* Match Navbar total height including borders/padding */
		/* padding-top: 88px; */
	}
</style>

<main class="bg-gradient-to-b from-black to-gray-900 text-white dm-sans ">
	<Navbar />
	<div class="app-content">
		{@render children()}
	</div>
	<Footer />
</main>
