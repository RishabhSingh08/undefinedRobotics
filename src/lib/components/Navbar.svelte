<script>
  import IconLogo from "../images/logo.png";
  import AdBanner from "../images/sponsors/AdBanner.png";
  let mobileMenuOpen = false;
</script>

<style>
  .dm-sans {
    font-family: "DM Sans", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
  }
</style>

<nav class="fixed top-0 left-0 right-0 z-50 px-4 py-4 dm-sans backdrop-blur-lg text-sm border-white/20 border-b">
  <div class="max-w-7xl mx-auto flex items-center justify-between">
    <a href="/" class="flex items-center space-x-3 group">
      <img src={IconLogo} alt="Undefined Robotics Logo" class="h-12 w-12" />
    </a>

    <!-- Desktop Nav -->
    <div class="hidden md:flex items-center space-x-8">
      <a href="/family" class="text-white hover:text-yellow-400 transition-colors duration-200 relative group">
        Our Family
        <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
      </a>
      <a href="/robot" class="text-white hover:text-yellow-400 transition-colors duration-200 relative group">
        Robots
        <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
      </a>
      <a href="/impact" class="text-white hover:text-yellow-400 transition-colors duration-200 relative group">
        Impact
        <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
      </a>
      <a href="/record" class="text-white hover:text-yellow-400 transition-colors duration-200 relative group">
        Record
        <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
      </a>
      <a href="/contact" class="text-white hover:text-yellow-400 transition-colors duration-200 relative group">
        Contact
        <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
      </a>
      <a href="/donate" class="text-white hover:text-yellow-400 transition-colors font-bold duration-200 relative group">
        Donate
        <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
      </a>
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
        <a href="/family" class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2" on:click={() => mobileMenuOpen = false}>Our Family</a>
        <a href="/robot" class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2" on:click={() => mobileMenuOpen = false}>Robots</a>
        <a href="/impact" class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2" on:click={() => mobileMenuOpen = false}>Impact</a>
        <a href="/record" class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2" on:click={() => mobileMenuOpen = false}>Record</a>
        <a href="/contact" class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2" on:click={() => mobileMenuOpen = false}>Contact</a>
        <a href="/donate" class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2 font-bold" on:click={() => mobileMenuOpen = false}>Donate</a>
        
        <!-- Divider -->
        <div class="border-t border-white/20 pt-4">
          <div class="flex justify-center">
            <img 
              src={AdBanner} 
              alt="Sponsor Banner" 
              class="h-12 w-auto rounded-lg opacity-100"
            />
          </div>
        </div>
      </div>
    </div>
  {/if}
</nav>
