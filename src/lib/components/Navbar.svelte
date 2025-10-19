<script>
  import { page } from '$app/stores';
  import IconLogo from "../images/logo.png";
  import AdBanner from "../images/sponsors/AdBanner.png";
  let mobileMenuOpen = false;

  const navLinks = [
    { href: '/family', label: 'Our Family', bold: false },
    { href: '/robot', label: 'Robots', bold: false },
    { href: '/impact', label: 'Impact', bold: false },
    { href: '/record', label: 'Record', bold: false },
    { href: '/contact', label: 'Contact', bold: false },
    { href: '/donate', label: 'Donate', bold: false }
  ];

  $: currentPath = $page.url.pathname;
</script>

<style>
  .dm-sans {
    font-family: "DM Sans", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
  }
</style>

<nav class="fixed top-0 left-0 right-0 z-50 dm-sans backdrop-blur-lg text-xl border-white/20 border-b">
  <div class="max-w-7xl mx-auto px-4 py-4 flex items-center justify-between relative">
    <a href="/" class="flex items-center space-x-3 group">
      <img src={IconLogo} alt="Undefined Robotics Logo" class="h-12 w-12" />
    </a>

    <!-- Desktop Nav -->
    <div class="hidden md:flex items-center space-x-8 relative">
      {#each navLinks as link}
        <a href={link.href} class="relative group py-4 text-white">
          <span class="relative">
            {link.label}
            <span class="absolute left-0 -bottom-1 w-0 h-0.5 bg-gradient-to-r from-yellow-400 to-yellow-200 transition-all duration-200 group-hover:w-full"></span>
          </span>
        </a>
      {/each}
    </div>

    <!-- Mobile Button -->
    <button class="md:hidden text-white p-2" on:click={() => mobileMenuOpen = !mobileMenuOpen}>
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        {#if mobileMenuOpen}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        {:else}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        {/if}
      </svg>
    </button>
  </div>

  <!-- Mobile Menu -->
  {#if mobileMenuOpen}
    <div class="md:hidden mt-4 backdrop-blur-sm rounded-lg border border-white/10">
      <div class="px-6 py-4 space-y-4">
        {#each navLinks as link}
          <a href={link.href} class="block text-white hover:bg-gradient-to-r hover:from-yellow-400 hover:to-yellow-200 hover:bg-clip-text hover:text-transparent transition-all duration-200 py-2 {link.bold ? 'font-bold' : ''}" on:click={() => mobileMenuOpen = false}>{link.label}</a>
        {/each}
        
        <!-- Divider -->
        <div class="border-t border-white/20 pt-4">
          <div class="flex justify-center">
            <img 
              src={AdBanner} 
              alt="Sponsor Banner" 
              class="h-auto max-h-16 w-auto rounded-lg"
            />
          </div>
        </div>
      </div>
    </div>
  {/if}
</nav>
