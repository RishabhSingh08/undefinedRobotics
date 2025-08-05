<!-- OG DONATION PAGE -->

<script>
  import { writable, derived } from 'svelte/store';
    import IconLogo from "../../lib/images/logo.png";


  // Props
  
  // Form state
  let name = "";
  let email = "";
  let amount = "";
  let showError = false;
  let formErrors = {};

  function validateForm() {
    formErrors = {
      name: !name.trim() && "Name is required",
      email: !email.trim() && "Email is required",
      amount: (!amount || parseFloat(amount) <= 0) && "Valid amount is required"
    };
    return !Object.values(formErrors).some(Boolean);
  }

  function generateDonationLink() {
    if (!validateForm()) {
      showError = true;
      return null;
    }
    const params = new URLSearchParams({
      name: name,
      email: email,
      message: `Total Donation: $${amount}`,
      amount: (parseFloat(amount) * 100).toFixed(0)
    });
    return `https://hcb.hackclub.com/donations/start/undefined-robotics?${params.toString()}`;
  }

  function handleSubmit(event) {
    event.preventDefault();
    const link = generateDonationLink();
    if (link) window.location.href = link;
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

<main class="text-white overflow-hidden relative dm-sans min-h-screen">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <div class="relative z-10 pt-32 pb-16 min-h-screen flex items-center justify-center px-4">
    <div class="max-w-lg mx-auto w-full">
      <div class="bg-[#10141c] border border-white/20 rounded-xl p-8 space-y-8">
        
        <div class="text-center space-y-4">
          {#if IconLogo}
            <img src={IconLogo} alt="Organization Logo" class="h-24 mx-auto" />
          {/if}
          
          <h1 class="text-3xl md:text-4xl font-bold tracking-wide">
            Make a Donation
          </h1>
          <p class="text-lg text-gray-300 leading-relaxed">
            Support our mission to inspire the next generation through robotics and STEM education.
          </p>
        </div>

        <form on:submit={handleSubmit} class="space-y-6">
          <div class="space-y-2">
            <label for="name" class="block text-sm font-medium text-gray-300">
              Name
            </label>
            <input
              id="name"
              type="text"
              bind:value={name}
              class="w-full px-4 py-3 bg-white/5 border border-white/20 rounded-lg text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none transition-colors {formErrors.name ? 'border-yellow-500' : ''}"
              placeholder="Your name"
            />
            {#if formErrors.name && showError}
              <p class="text-yellow-400 text-sm">{formErrors.name}</p>
            {/if}
          </div>

          <div class="space-y-2">
            <label for="email" class="block text-sm font-medium text-gray-300">
              Email
            </label>
            <input
              id="email"
              type="email"
              bind:value={email}
              class="w-full px-4 py-3 bg-white/5 border border-white/20 rounded-lg text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none transition-colors {formErrors.email ? 'border-yellow-500' : ''}"
              placeholder="your@email.com"
            />
            {#if formErrors.email && showError}
              <p class="text-yellow-400 text-sm">{formErrors.email}</p>
            {/if}
          </div>

          <div class="space-y-3">
            <label for="amount" class="block text-sm font-medium text-gray-300">
              Amount (USD)
            </label>
            
            <div class="grid grid-cols-4 gap-2">
              {#each [25, 50, 100, 250] as quickAmount}
                <button
                  type="button"
                  on:click={() => amount = quickAmount}
                  class="px-3 py-2 bg-white/5 border border-white/20 rounded-lg text-white hover:bg-white/10 transition-colors {amount == quickAmount ? 'bg-yellow-500/20 border-yellow-500' : ''}"
                >
                  ${quickAmount}
                </button>
              {/each}
            </div>

            <div class="relative">
              <span class="absolute left-3 top-1/2 transform -translate-y-1/2 text-gray-400">$</span>
              <input
                id="amount"
                type="number"
                bind:value={amount}
                min="0"
                step="0.01"
                class="w-full pl-8 pr-4 py-3 bg-white/5 border border-white/20 rounded-lg text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none transition-colors {formErrors.amount ? 'border-yellow-500' : ''}"
                placeholder="Custom amount"
              />
            </div>
            
            {#if formErrors.amount && showError}
              <p class="text-yellow-400 text-sm">{formErrors.amount}</p>
            {/if}
          </div>

          <button
            type="submit"
            class="w-full px-6 py-3 bg-yellow-500 text-black font-semibold rounded-lg hover:bg-yellow-400 focus:outline-none focus:ring-2 focus:ring-yellow-500 transition-colors group"
          >
            Donate Now
            <span class="inline-block transition-transform group-hover:translate-x-1 ml-2">→</span>
          </button>

          {#if showError && Object.values(formErrors).some(Boolean)}
            <p class="text-center text-yellow-400 text-sm">
              Please fill in all required fields correctly
            </p>
          {/if}
        </form>


      </div>
    </div>
  </div>
</main>