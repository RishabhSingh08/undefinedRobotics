<script>
  import { page } from '$app/stores';
  import { goto } from '$app/navigation';
  import IconLogo from "../images/logo.png";
  import AdBanner from "../images/sponsors/AdBanner.png";
  let mobileMenuOpen = false;
  let searchOpen = false;
  let searchQuery = '';

  const navLinks = [
    { href: '/family', label: 'Our Family', bold: false },
    { href: '/robot', label: 'Robots', bold: false },
    { href: '/impact', label: 'Impact', bold: false },
    { href: '/record', label: 'Record', bold: false },
    { href: '/contact', label: 'Contact', bold: false },
    { href: '/donate', label: 'Donate', bold: false }
  ];

  const searchableContent = [
    { 
      title: 'Home', 
      path: '/', 
      description: 'Main landing page',
      keywords: ['mission', 'serve underserved', 'robotics', 'team', 'events', 'sponsors', 'undefined', 'stem', 'ftc', 'dallas', 'fort worth', 'texas', 'plano', 'nonprofit', '501c3', 'engineering', 'education', 'community', 'outreach']
    },
    { 
      title: 'Our Family - Team Members', 
      path: '/family', 
      description: 'Meet our team leadership and members',
      keywords: ['team', 'members', 'chiefs', 'leadership', 'missing amps', 'undefined', 'akshat kumar', 'punit lakhotiya', 'rishabh singh', 'swaraj nibandhe', 'nishant sinari', 'neel tipnis', 'lucas silva', 'erik wang', 'xander kuksov', 'navin rao', 'samanyu earna', 'azalea tang', 'ainesh gupta', 'ashwin gupta', 'mahit cherku', 'vedant teware', 'captain', 'cfo', 'cto', 'coo', 'executive director', 'plano west', 'plano senior', 'jasper', '25782', '30801']
    },
    { 
      title: 'Robots - InfiNemo', 
      path: '/robot', 
      description: 'Our FTC competition robot',
      keywords: ['infinemo', 'ftc', 'competition', 'robot', 'intake', 'chassis', 'arm', 'into the deep', 'autonomous', 'teleop', 'claw', 'linear extension', 'mecanum wheels', 'odometry', 'limelight', 'specimens', 'samples', 'drive system', 'scoring', '3dof', 'axon', 'fusion 360', 'cad', 'aluminum', 'misumi', 'linear slides']
    },
    { 
      title: 'Impact - Community Outreach', 
      path: '/impact', 
      description: 'Our STEM outreach and community programs',
      keywords: ['outreach', 'mentorship', 'community', 'events', 'stem', 'education', '3d print showcase', 'smart seniors', 'environmental workshop', 'girls coding classes', 'career literacy', 'tribal communities', 'south asia', 'robotics program', 'climate change', 'shanti bhavan', 'underserved', 'video series', 'workshops', 'naihati', 'india', 'orphanage', 'tedx', 'engagement', '3000']
    },
    { 
      title: 'Record - Awards & Achievements', 
      path: '/record', 
      description: 'Competition awards and team achievements',
      keywords: ['awards', 'achievements', 'competitions', 'championships', 'wins', 'control award', 'rtx innovate', 'connect award', 'finalist', 'winning alliance', 'design award', 'inspire award', 'texas ftc', 'fit-north', 'pre-worlds', 'state championship', 'uil', 'regional', 'national', 'sapphire division', 'area championship', 'transparency', 'irs', '501c3', 'hack foundation', 'candid', 'fiscal sponsorship']
    },
    { 
      title: 'Contact Us', 
      path: '/contact', 
      description: 'Get in touch with our team',
      keywords: ['contact', 'email', 'instagram', 'discord', 'message', 'reach out', 'sponsor', 'partnership', 'volunteer', 'position', 'undefinedrobotics', 'contact@undefinedrobotics.org', 'plano texas', 'location', 'social media']
    },
    { 
      title: 'Donate & Support', 
      path: '/donate', 
      description: 'Support our mission with a donation',
      keywords: ['donate', 'sponsorship', 'support', 'contribution', 'funding', 'tax deductible', 'platinum', 'gold', 'silver', 'partner', 'hcb', 'hack club bank', 'nonprofit', 'charitable', 'give', 'sponsorship package', 'financial support']
    },
    { 
      title: 'Privacy Policy', 
      path: '/privacy-policy', 
      description: 'Our privacy and data protection policy',
      keywords: ['privacy', 'policy', 'data', 'security', 'vercel analytics', 'information', 'contact form', 'protection']
    },
  ];

  $: currentPath = $page.url.pathname;
  
  $: filteredResults = searchQuery.trim() 
    ? searchableContent.filter(item => {
        const query = searchQuery.toLowerCase();
        return item.title.toLowerCase().includes(query) ||
               item.description.toLowerCase().includes(query) ||
               item.keywords.some(keyword => keyword.toLowerCase().includes(query));
      }).slice(0, 8)
    : [];

  function handleSearch(result) {
    goto(result.path);
    searchQuery = '';
    searchOpen = false;
  }

  function handleSearchKeydown(event) {
    if (event.key === 'Escape') {
      searchOpen = false;
      searchQuery = '';
    }
  }

  function handleClickOutside(event) {
    if (searchOpen && !event.target.closest('.search-container') && !event.target.closest('.search-button')) {
      searchOpen = false;
      searchQuery = '';
    }
  }
</script>

<style>
  .dm-sans {
    font-family: "DM Sans", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
  }
</style>

<svelte:window on:click={handleClickOutside} />

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
      
      <!-- Search Button -->
      <button 
        class="search-button text-white p-2 hover:text-yellow-400 transition-colors"
        on:click={() => searchOpen = !searchOpen}
        aria-label="Search"
      >
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg>
      </button>
    </div>

    <!-- Mobile Buttons -->
    <div class="md:hidden flex items-center space-x-2">
      <button 
        class="search-button text-white p-2 hover:text-yellow-400 transition-colors"
        on:click={() => searchOpen = !searchOpen}
        aria-label="Search"
      >
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg>
      </button>
      
      <button class="text-white p-2" on:click={() => mobileMenuOpen = !mobileMenuOpen}>
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          {#if mobileMenuOpen}
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          {:else}
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          {/if}
        </svg>
      </button>
    </div>
  </div>

  <!-- Search Modal -->
  {#if searchOpen}
    <div class="search-container absolute top-full left-0 right-0 mt-2 mx-4 backdrop-blur-lg bg-gray-900/95 border border-white/20 rounded-lg shadow-2xl z-50">
      <div class="p-4">
        <div class="relative">
          <input
            type="text"
            bind:value={searchQuery}
            on:keydown={handleSearchKeydown}
            placeholder="Search pages..."
            class="w-full bg-gray-800 text-white px-4 py-3 pl-10 rounded-lg border border-white/20 focus:border-yellow-400 focus:outline-none focus:ring-2 focus:ring-yellow-400/50"
            autofocus
          />
          <svg class="w-5 h-5 absolute left-3 top-1/2 transform -translate-y-1/2 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
        </div>
        
        {#if searchQuery.trim() && filteredResults.length > 0}
          <div class="mt-3 space-y-1 max-h-96 overflow-y-auto">
            {#each filteredResults as result}
              <button
                class="w-full text-left px-4 py-3 rounded-lg hover:bg-gray-800 transition-colors text-white group"
                on:click={() => handleSearch(result)}
              >
                <div class="font-semibold group-hover:text-yellow-400 transition-colors">{result.title}</div>
                <div class="text-sm text-gray-400 mt-1">{result.description}</div>
              </button>
            {/each}
          </div>
        {:else if searchQuery.trim()}
          <div class="mt-3 px-4 py-3 text-gray-400 text-sm">
            No results found for "{searchQuery}"
          </div>
        {/if}
      </div>
    </div>
  {/if}

  <!-- Mobile Menu -->
  {#if mobileMenuOpen}
    <div class="md:hidden mt-4 backdrop-blur-sm rounded-lg border border-white/10">
      <div class="px-6 py-4 space-y-4">
        {#each navLinks as link}
          <a href={link.href} class="block text-white hover:bg-gradient-to-r hover:from-yellow-400 hover:to-yellow-200 hover:bg-clip-text hover:text-transparent transition-all duration-200 py-2 {link.bold ? 'font-bold' : ''}" on:click={() => mobileMenuOpen = false}>{link.label}</a>
        {/each}
        
        <!-- Divider -->
        </div>
    </div>
  {/if}
</nav>
