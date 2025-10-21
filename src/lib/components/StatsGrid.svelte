<script>
  let showModal = false;
  
  const breakdownData = [
    { category: 'Gift Matching Donations', amount: '$11,700' },
    { category: 'Grants (Government, FIRST, etc.)', amount: '$8,250' },
    { category: 'Sponsorships/Partnerships', amount: '$8,967' },
    { category: 'Team services & setup', amount: '$11,600' }
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
    { value: '42', label: 'Professionals Connected' }
  ];
  
  function openModal() {
    showModal = true;
  }
  
  function closeModal() {
    showModal = false;
  }
</script>

<div class="grid grid-cols-2 md:grid-cols-5 gap-8">
  {#each stats as stat, index}
    <div class="text-center {index === stats.length - 1 ? 'col-span-2 md:col-span-1' : ''}">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">
        {stat.value}
      </div>
      {#if index === 0}
        <button 
          class="text-gray-300 underline cursor-pointer border-0 bg-transparent p-0 hover:text-gray-100 transition-colors"
          on:click={openModal}
        >
          {stat.label}
        </button>
      {:else}
        <div class="text-gray-300">{stat.label}</div>
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
