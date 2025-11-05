<script>
  let showModal = false;
  let showUnderservedModal = false;
  
  const breakdownData = [
    { category: 'Gift Matching Donations', amount: '$11,700' },
    { category: 'Grants (Government, FIRST, etc.)', amount: '$8,250' },
    { category: 'Sponsorships/Partnerships', amount: '$8,967' },
    { category: 'Team services & setup', amount: '$11,600' }
  ];
  
  const underservedData = [
    { name: 'International Girls Robotics Program', base: 15, multiplier: 1.5, adjusted: 22.5 },
    { name: 'Spreading FIRST to Tribes in South Asia', base: 40, multiplier: 1.5, adjusted: 60.0 },
    { name: 'STEM Sticker Delivery (Shanti Bhavan)', base: 150, multiplier: 0.5, adjusted: 75.0 },
    { name: 'Weekly Girls Coding Classes', base: 25, multiplier: 1.5, adjusted: 37.5 },
    { name: '3D Print Showcase', base: 200, multiplier: 1.0, adjusted: 200.0 },
    { name: 'Smart Seniors (Video Series)', base: 300, multiplier: 0.25, adjusted: 75.0 },
    { name: 'Autonomic Robots for Climate Change', base: 20, multiplier: 1.5, adjusted: 30.0 },
    { name: 'Titkok - Autonomic Robotics for Climates', base: 6000, multiplier: 0.25, adjusted: 1500.0 },
    { name: 'Career Literacy Program', base: 5000, multiplier: 0.25, adjusted: 1250.0 },
    { name: 'Environmental Sustainability Workshop', base: 50, multiplier: 1.0, adjusted: 50.0 }
  ];
  
  // Calculate total value raised from breakdown data
  function calculateTotalValue() {
    const total = breakdownData.reduce((sum, item) => {
      // Remove $ and commas, then parse as number
      const amount = parseFloat(item.amount.replace(/[$,]/g, ''));
      return sum + amount;
    }, 0);
    
    // Format as K (thousands) with one decimal place
    const totalInK = (total / 1000).toFixed(1);
    return `$${totalInK}K+`;
  }
  
  const stats = [
    { value: calculateTotalValue(), label: 'Value Raised' },
    { value: '3,000+', label: 'Underserved Individuals Reached' },
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
    <div class="flex flex-col items-center text-center">
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
<!-- Modal -->
<!-- Modal -->
{#if showModal}
  <div 
    class="fixed inset-0 bg-black/40 backdrop-blur-sm flex items-center justify-center z-50 p-4"
    on:click={closeModal}
    on:keydown={(e) => e.key === 'Escape' && closeModal()}
    role="button"
    tabindex="-1"
  >
    <div 
      class="bg-gray-900 rounded-lg p-6 max-w-md w-full shadow-2xl border border-yellow-500/30"
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

      <p class="text-gray-400 text-sm mb-3">Sectors of Funding and Savings to Date:</p>

      <div class="flex flex-col space-y-2 mb-4">
        {#each breakdownData as item}
          <div class="flex justify-between items-center bg-gray-800/60 rounded-md px-3 py-2">
            <span class="text-gray-300 text-sm">{item.category}</span>
            <span class="text-yellow-400 font-semibold">{item.amount}</span>
          </div>
        {/each}
      </div>

      <div class="border-t border-gray-700 mt-2 mb-3"></div>

      <div class="flex justify-between items-center text-lg font-bold">
        <span class="text-white">Total Value</span>
        <span class="bg-gradient-to-r from-yellow-400 to-yellow-200 bg-clip-text text-transparent text-2xl">$40.5K</span>
      </div>

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
    <div 
      class="bg-gray-900 rounded-lg p-6 max-w-md w-full shadow-2xl border border-yellow-500/30"
      on:click={(e) => e.stopPropagation()}
      role="dialog"
      tabindex="-1"
    >
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-xl font-bold text-white">Underserved Individuals Reached</h2>
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
        <p>• Video / Media: 0.25</p>
      </div>

    </div>
  </div>
{/if}
