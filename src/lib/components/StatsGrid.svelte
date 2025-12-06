<script>
  let showModal = false;
  let showUnderservedModal = false;
  
  const grantSources = [
    { name: '24-25: Gift Matching', amount: '$3,600.00', date: '12/12/2024' },
    { name: '24-25: Texas Workforce Commission', amount: '$1,500.00', date: '8/4/2025' },
    { name: '24-25: Hardship Grant', amount: '$750.00', date: '10/13/2024' },
    { name: '24-25: Argosy FTC SIM Canada', amount: '$1,000.00', date: '9/2/2024' },
    { name: '25-26: Gift Matching', amount: '$3,949.00', date: '10/3/2025' },
    { name: '25-26: GENE HAAS', amount: '$2,000.00', date: '10/21/2025' },
    { name: '25-26: Hack Club Bank: Starting Amount', amount: '$150.00', date: '7/1/2025' },
    { name: '25-26: Leidos', amount: '$1,083.00', date: '7/1/2025' },
    { name: '25-26: GENE HAAS - Missing Amps', amount: '$2,000.00', date: '9/23/2025' }
  ];
  
  const sponsorshipSources = [
    { name: '24-25: Cafelli Technologies', amount: '$1,000.00', date: '11/3/2024' },
    { name: '24-25: Polymaker', amount: '$400.00', date: '10/27/2024' },
    { name: '25-26: Build Live', amount: '$5,467.00', date: '10/1/2025' },
    { name: '25-26: Team Fees', amount: '$3,008.01', date: '7/16/2025' },
    { name: '25-26: Satya Karri', amount: '$100.00', date: '7/31/2025' },
    { name: '25-26: Parts carried on', amount: '$4,500.00', date: '' },
    { name: '25-26: Team parts Robotics Parts and Services', amount: '$10,143.00', date: '' }
  ];
  
  const underservedData = [
    { name: 'International Girls Robotics Program', base: 15, multiplier: 1.5, adjusted: 22.5 },
    { name: 'Spreading FIRST to Tribes in South Asia', base: 40, multiplier: 1.5, adjusted: 60.0 },
    { name: 'STEM Sticker Delivery (Shanti Bhavan)', base: 150, multiplier: 0.5, adjusted: 75.0 },
    { name: 'Weekly Girls Coding Classes', base: 25, multiplier: 1.5, adjusted: 37.5 },
    { name: '3D Print Showcase', base: 200, multiplier: 1.0, adjusted: 200.0 },
    { name: 'Smart Seniors (Video Series)', base: 300, multiplier: 0.1, adjusted: 30.0 },
    { name: 'Autonomic Robots for Climate Change', base: 20, multiplier: 1.5, adjusted: 30.0 },
    { name: 'TikTok - Autonomic Robotics for Climates', base: 6750, multiplier: 0.1, adjusted: 675.0 },
    { name: 'Career Literacy Program', base: 5000, multiplier: 0.1, adjusted: 500.0 },
    { name: 'Environmental Sustainability Workshop', base: 50, multiplier: 1.0, adjusted: 50.0 },
    { name: 'Build Show Live 2025', base: 5400, multiplier: 0.3, adjusted: 1620.0 }
  ];
  
  // Calculate totals
  function calculateTotal(sources) {
    return sources.reduce((sum, item) => {
      const amount = parseFloat(item.amount.replace(/[$,]/g, ''));
      return sum + amount;
    }, 0);
  }
  
  function formatCurrency(value) {
    return new Intl.NumberFormat('en-US', {
      style: 'currency',
      currency: 'USD',
      minimumFractionDigits: 2
    }).format(value);
  }
  
  const totalGrants = calculateTotal(grantSources);
  const totalSponsors = calculateTotal(sponsorshipSources);
  const totalRaised = totalGrants + totalSponsors;
  
  function calculateTotalValue() {
    const totalInK = (Math.floor((totalRaised / 1000) * 10) / 10).toFixed(1);
    return `$${totalInK}K+`;
  }
  
  const stats = [
    { value: calculateTotalValue(), label: 'Value Raised' },
    { value: '3,300+', label: 'Underserved Engagement' },
    { value: '36', label: 'FTC Teams Connected' },
    { value: '12', label: 'Regional/National Awards' },
    { value: '102', label: 'Professionals Connected' },
  ];
  
  function openModal() {
    showModal = true;
  }
  
  function closeModal() {
    showModal = false;
  }
  
  function openUnderservedModal() {
    showUnderservedModal = true;
  }
  
  function closeUnderservedModal() {
    showUnderservedModal = false;
  }
</script>

<div class="grid grid-cols-2 sm:grid-cols-2 md:grid-cols-5 gap-8">
  {#each stats as stat, index}
    <div class="flex flex-col items-center text-center animate-fade-up animate-delay-{index * 100}">  
        <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">
        {stat.value}
      </div>

      {#if index === 0}
        <button 
          class="text-gray-300 underline cursor-pointer border-0 bg-transparent p-0 hover:text-gray-100 transition-colors text-sm md:text-base"
          on:click={openModal}
        >
          {stat.label}
        </button>
      {:else if index === 1}
        <button 
          class="text-gray-300 underline cursor-pointer border-0 bg-transparent p-0 hover:text-gray-100 transition-colors text-sm md:text-base"
          on:click={openUnderservedModal}
        >
          {stat.label}
        </button>
      {:else}
        <div class="text-gray-300 text-sm md:text-base">{stat.label}</div>
      {/if}
    </div>
  {/each}
</div>

<!-- Contributions Overview Modal -->
{#if showModal}
  <div 
    class="fixed inset-0 bg-black/40 backdrop-blur-sm flex items-center justify-center z-50 p-4"
    on:click={closeModal}
    on:keydown={(e) => e.key === 'Escape' && closeModal()}
    role="button"
    tabindex="-1"
  >
    <!-- svelte-ignore a11y_click_events_have_key_events -->
    <div 
      class="bg-gray-900 rounded-lg p-6 max-w-2xl w-full shadow-2xl border border-yellow-500/30 max-h-[90vh] overflow-y-auto"
      on:click={(e) => e.stopPropagation()}
      role="dialog"
      tabindex="-1"
    >
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-xl font-bold text-white">Contributions Overview</h2>
        <button 
          on:click={closeModal}
          class="text-gray-400 hover:text-white hover:cursor-pointer transition-colors text-2xl"
          aria-label="Close modal"
        >
          ×
        </button>
      </div>

      <div class="border-t border-gray-700 mb-4"></div>

      <!-- Total Summary Boxes -->
      <div class="grid grid-cols-3 gap-3 mb-4">
        <div class="bg-green-900/20 border border-green-500/30 rounded-md p-3 text-center">
          <div class="text-xs text-gray-400 mb-1">Total Grants</div>
          <div class="text-lg font-bold text-green-400">{formatCurrency(totalGrants)}</div>
        </div>
        <div class="bg-blue-900/20 border border-blue-500/30 rounded-md p-3 text-center">
          <div class="text-xs text-gray-400 mb-1">Total Sponsors</div>
          <div class="text-lg font-bold text-blue-400">{formatCurrency(totalSponsors)}</div>
        </div>
        <div class="bg-yellow-900/20 border border-yellow-500/30 rounded-md p-3 text-center">
          <div class="text-xs text-gray-400 mb-1">Total Raised</div>
          <div class="text-lg font-bold text-yellow-400">{formatCurrency(totalRaised)}</div>
        </div>
      </div>

      <!-- Grant Sources -->
      <div class="mb-4">
        <h3 class="text-green-400 font-semibold mb-2 flex items-center gap-2">
          <div class="w-3 h-3 bg-green-400 rounded-full"></div>
          Grant Sources
        </h3>
        <div class="flex flex-col space-y-1.5">
          {#each grantSources as item}
            <div class="flex justify-between items-center bg-gray-800/60 rounded-md px-3 py-2">
              <span class="text-gray-300 text-sm">{item.name}</span>
              <span class="text-green-400 font-semibold text-sm">{item.amount}</span>
            </div>
          {/each}
        </div>
      </div>

      <!-- Sponsorship Sources -->
      <div class="mb-4">
        <h3 class="text-blue-400 font-semibold mb-2 flex items-center gap-2">
          <div class="w-3 h-3 bg-blue-400 rounded-full"></div>
          Sponsorship Sources
        </h3>
        <div class="flex flex-col space-y-1.5">
          {#each sponsorshipSources as item}
            <div class="flex justify-between items-center bg-gray-800/60 rounded-md px-3 py-2">
              <span class="text-gray-300 text-sm">{item.name}</span>
              <span class="text-blue-400 font-semibold text-sm">{item.amount}</span>
            </div>
          {/each}
        </div>
      </div>

      <div class="border-t border-gray-700 mt-4 mb-3"></div>

      <div class="flex justify-between items-center text-lg font-bold mb-4">
        <span class="text-white">Total Value</span>
        <span class="bg-gradient-to-r from-yellow-400 to-yellow-200 bg-clip-text text-transparent text-2xl">{formatCurrency(totalRaised)}</span>
      </div>

      <a 
        href="https://docs.google.com/spreadsheets/d/1qDcwu3IL-yFm5ke4N2TmhjPN0Sr_KaEwJxRXgPcNs78/edit?gid=0#gid=0"
        target="_blank"
        rel="noopener noreferrer"
        class="inline-flex items-center gap-2 underline text-yellow-400 hover:text-yellow-300 transition-colors text-sm"
      >
        View detailed finances spreadsheet
        <i class="fa-solid fa-up-right-from-square"></i>
      </a>

    </div>
  </div>
{/if}

<!-- Underserved Individuals Modal -->
{#if showUnderservedModal}
  <div 
    class="fixed inset-0 bg-black/40 backdrop-blur-sm flex items-center justify-center z-50 p-4"
    on:click={closeUnderservedModal}
    on:keydown={(e) => e.key === 'Escape' && closeUnderservedModal()}
    role="button"
    tabindex="-1"
  >
    <!-- svelte-ignore a11y_click_events_have_key_events -->
    <div 
      class="bg-gray-900 rounded-lg p-6 max-w-md w-full shadow-2xl border border-yellow-500/30"
      on:click={(e) => e.stopPropagation()}
      role="dialog"
      tabindex="-1"
    >
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-xl font-bold text-white">Underserved Engagement</h2>
        <button 
          on:click={closeUnderservedModal}
          class="text-gray-400 hover:text-white hover:cursor-pointer transition-colors text-2xl"
          aria-label="Close modal"
        >
          ×
        </button>
      </div>

      <div class="border-t border-gray-700 mb-4"></div>

      <p class="text-gray-400 text-sm mb-3">Individual project impact calculations:</p>

      <div class="flex flex-col space-y-2 mb-4 max-h-60 overflow-y-auto">
        {#each underservedData as project}
          <div class="flex justify-between items-center bg-gray-800/60 rounded-md px-3 py-2">
            <span class="text-gray-300 text-sm flex-1 mr-2">{project.name}</span>
            <span class="text-gray-400 text-sm whitespace-nowrap">{project.base} × {project.multiplier} = <span class="text-yellow-400 font-medium">{project.adjusted}</span></span>
          </div>
        {/each}
      </div>

      <div class="border-t border-gray-700 mt-2 mb-3"></div>

      <div class="flex justify-between items-center text-lg font-bold mb-3">
        <span class="text-white">Total Individuals Reached</span>
        <span class="bg-gradient-to-r from-yellow-400 to-yellow-200 bg-clip-text text-transparent text-2xl">3,300</span>
      </div>

      <div class="text-xs text-gray-400">
        <p class="mb-1"><strong>Multiplier Key:</strong></p>
        <p>• Reinforced: 1.5</p>
        <p>• Hands-On: 1.0</p>
        <p>• Community / Outreach: 0.5</p>
        <p>• Expo / Large Event: 0.3</p>
        <p>• Video / Media: 0.1</p>
      </div>

    </div>
  </div>
{/if}