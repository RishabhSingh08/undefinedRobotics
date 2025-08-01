<!-- Navbar.svelte -->
<script>
    import IconLogo from "../images/logo.png";
    
    let mobileMenuOpen = false;
    
    const navItems = [
      { name: 'Our Family', href: '/family' },
      { name: 'Contact', href: '/contact' },
      { name: 'Impact', href: '/impact' },
      { name: 'Record', href: '/record' }
    ];
  </script>
  
  <style>
    .dm-sans {
      font-family: "DM Sans", sans-serif;
      font-optical-sizing: auto;
      font-weight: 400;
      font-style: normal;
    }
  </style>
  
  <nav class="fixed top-0 left-0 right-0 z-50 px-4 py-4 dm-sans backdrop-blur-xl text-lg  border-white/20 border-b">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
      <a href="/" class="flex items-center space-x-3 group">
        <img src={IconLogo} alt="Undefined Robotics Logo" class="h-12 w-12" />
      </a>
      
      <div class="hidden md:flex items-center space-x-8">
        {#each navItems as item}
          <a 
            href={item.href} 
            class="text-white hover:text-yellow-400 transition-colors duration-200 relative group"
          >
            {item.name}
            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-yellow-400 transition-all duration-200 group-hover:w-full"></span>
          </a>
        {/each}
      </div>
      
      <button 
        class="md:hidden text-white p-2"
        on:click={() => mobileMenuOpen = !mobileMenuOpen}
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          {#if mobileMenuOpen}
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          {:else}
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          {/if}
        </svg>
      </button>
    </div>
    
    {#if mobileMenuOpen}
      <div class="md:hidden mt-4 bg-black/95 backdrop-blur-sm rounded-lg border border-white/10">
        <div class="px-6 py-4 space-y-4">
          {#each navItems as item}
            <a 
              href={item.href} 
              class="block text-white hover:text-yellow-400 transition-colors duration-200 py-2"
              on:click={() => mobileMenuOpen = false}
            >
              {item.name}
            </a>
          {/each}
        </div>
      </div>
    {/if}
  </nav>
  