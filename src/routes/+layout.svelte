<!-- +layout.svelte (SEO-optimized) -->
<script>
  import '../app.css';
  import Navbar from '../lib/components/Navbar.svelte';
  import Footer from '../lib/components/Footer.svelte';
  import { injectAnalytics } from '@vercel/analytics/sveltekit'
  injectAnalytics();

  let { children } = $props();
</script>

<svelte:head>
  <!-- Global SEO -->
  <meta name="theme-color" content="#000000" />

  <!-- Favicon -->
  <link rel="icon" href="/favicon.ico" />
  <link rel="apple-touch-icon" href="/apple-touch-icon.png" />
  <link rel="manifest" href="/site.webmanifest" />

  <!-- Global Organization Schema (safe because it's general) -->
  <script type="application/ld+json">
  {
    "@context": "http://schema.org",
    "@type": "NonprofitOrganization",
    "name": "Undefined Robotics",
    "url": "https://undefinedrobotics.org",
    "logo": "https://undefinedrobotics.org/logo.png",
    "description": "A student-led robotics 501(c)3 nonprofit providing STEM access to underserved communities.",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Dallas-Fort Worth",
      "addressRegion": "TX",
      "addressCountry": "US"
    }
  }
  </script>
</svelte:head>

<style>
  .dm-sans {
    font-family: "DM Sans", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
  }

  .app-content {}

  :global(*) {
    user-select: text;
    -webkit-user-select: text;
    -moz-user-select: text;
    -ms-user-select: text;
  }
</style>

<main class="bg-gradient-to-b from-black to-gray-900 text-white dm-sans">
  <Navbar />
  <div class="app-content">
    {@render children()}
  </div>
  <Footer />
</main>
