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

<main class="text-white overflow-hidden relative dm-sans">
  <!-- Background pattern for visual effect -->
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <!-- Main content container, centered on the screen -->
  <div class="relative z-10 min-h-screen flex justify-center px-6 py-32">
    <div class="max-w-3xl mx-auto w-full">
        
        
        <section class="relative z-10 px-4 space-y-8">
          <div class="max-w-7xl mx-auto text-center">
            <h1 class="text-4xl md:text-6xl font-semibold mb-8">
                  Make a Donation
            </h1>
            <p class="text-lg md:text-xl text-gray-400 max-w-3xl mx-auto">
                  Support our mission to inspire the next generation through robotics and STEM education.
            </p>
          </div>
            <div class="absolute top-1/4 left-10 w-24 h-24 bg-yellow-200 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob z-0"></div>
        <div class="absolute top-1/3 right-10 w-24 h-24 bg-yellow-500 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-2000 z-0"></div>
        <div class="absolute bottom-1/4 left-1/3 w-24 h-24 bg-yellow-700 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-4000 z-0"></div>
        </section>

        <!-- Donation form -->
        <form on:submit|preventDefault={handleSubmit} class="space-y-10">
          <!-- Name input field -->
          <div class="space-y-4">
            <label for="name" class="block text-xl font-medium text-gray-300">
              Name
            </label>
            <input
              id="name"
              type="text"
              bind:value={name}
              class="w-full px-6 py-5 bg-[#0f0e13] border border-white/20 rounded-lg text-xl text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none transition-colors {formErrors.name ? 'border-yellow-500' : ''}"
              placeholder="Your name"
            />
            {#if formErrors.name && showError}
              <p class="text-yellow-400 text-lg mt-2">{formErrors.name}</p>
            {/if}
          </div>

          <!-- Email input field -->
          <div class="space-y-4">
            <label for="email" class="block text-xl font-medium text-gray-300">
              Email
            </label>
            <input
              id="email"
              type="email"
              bind:value={email}
              class="w-full px-6 py-5 bg-[#0f0e13] border border-white/20 rounded-lg text-xl text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none transition-colors {formErrors.email ? 'border-yellow-500' : ''}"
              placeholder="your@email.com"
            />
            {#if formErrors.email && showError}
              <p class="text-yellow-400 text-lg mt-2">{formErrors.email}</p>
            {/if}
          </div>

          <!-- Amount input and quick selection buttons -->
          <div class="space-y-5">
            <label for="amount" class="block text-xl font-medium text-gray-300">
              Amount (USD)
            </label>

            <!-- Quick amount selection buttons -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-5">
              {#each [25, 50, 100, 250] as quickAmount}
                <button
                  type="button"
                  on:click={() => amount = quickAmount}
                  class="px-6 py-4 bg-[#0f0e13] border border-white/20 rounded-lg text-xl text-white hover:bg-white/10 transition-colors {amount == quickAmount ? 'bg-yellow-500/20 border-yellow-500' : ''}"
                >
                  ${quickAmount}
                </button>
              {/each}
            </div>

            <!-- Custom amount input field -->
            <div class="relative">
              <span class="absolute left-5 top-1/2 transform -translate-y-1/2 text-gray-400 text-xl">$</span>
              <input
                id="amount"
                type="number"
                bind:value={amount}
                min="0"
                step="0.01"
                class="w-full pl-12 pr-6 py-5 bg-[#0f0e13] border border-white/20 rounded-lg text-xl text-white placeholder-gray-400 focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none transition-colors {formErrors.amount ? 'border-yellow-500' : ''}"
                placeholder="Custom amount"
              />
            </div>

            {#if formErrors.amount && showError}
              <p class="text-yellow-400 text-lg mt-2">{formErrors.amount}</p>
            {/if}
          </div>

          <!-- Donate Now button -->
          <button
            type="submit"
            class="w-full px-10 py-5 bg-yellow-500 text-black text-xl font-bold rounded-lg hover:bg-yellow-400 focus:outline-none focus:ring-2 focus:ring-yellow-500 transition-colors group shadow-lg hover:cursor-pointer"
          >
            Donate Now
            <span class="inline-block transition-transform group-hover:translate-x-1 ml-4 text-3xl">→</span>
          </button>

          <!-- General error message -->
          {#if showError && Object.values(formErrors).some(Boolean)}
            <p class="text-center text-yellow-400 text-lg">
              Please fill in all required fields correctly.
            </p>
          {/if}
        </form>
    </div>
  </div>
</main>