<script>
  import { writable, derived } from 'svelte/store';
    import IconLogo from "../../lib/images/logo.png";
    import SponsorshipPackage from "../../lib/images/Undefined Sponsorship Package.png";


  // Props
  
  // Form state
  let name = "";
  let email = "";
  let amount = "";
  let showError = false;
  let formErrors = {};
  let showSponsorshipPackage = false;

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

<svelte:head>
  <title>Undefined Robotics | Donate</title>
  <meta name="description" content="Support Undefined Robotics, a student-led 501(c)3 nonprofit. Your tax-deductible donation funds FTC robots, STEM outreach, and engineering education programs." />

  <link rel="canonical" href="https://undefinedrobotics.org/donate" />

  <meta property="og:title" content="Make a Donation to Undefined Robotics" />
  <meta property="og:description" content="Your tax-deductible contribution directly powers our robotics team, community outreach, and STEM educational efforts." />
  <meta property="og:image" content="/og-image.png" />
  <meta property="og:url" content="https://undefinedrobotics.org/donate" />
  <meta property="og:type" content="website" />

  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Support Undefined Robotics STEM Programs" />
  <meta name="twitter:description" content="Help fund our FTC robotics season and global STEM outreach programs with a tax-deductible donation." />
  <meta name="twitter:image" content="/og-image.png" />

  <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebPage",
      "name": "Donation Page",
      "description": "Page for making a charitable donation to Undefined Robotics, a 501(c)3 nonprofit organization.",
      "potentialAction": {
        "@type": "DonateAction",
        "name": "Donate Now",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://hcb.hackclub.com/donations/start/undefined-robotics",
          "actionStatus": "PotentialActionStatus"
        },
        "recipient": {
          "@type": "NonprofitOrganization",
          "name": "Undefined Robotics"
        }
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
</style>

<main class="text-white overflow-hidden relative dm-sans">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <div class="relative z-10 min-h-screen flex justify-center px-6 py-32">
    <div class="max-w-3xl mx-auto w-full">
        
        <section class="relative z-10 px-4 space-y-8 animate-fade-down">
          <div class="max-w-7xl mx-auto text-center">
            <h1 class="text-4xl md:text-6xl font-semibold mb-8">
              Make a Donation
            </h1>
          </div>
          <div class="absolute top-1/4 left-10 w-24 h-24 bg-yellow-200 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob z-0"></div>
          <div class="absolute top-1/3 right-10 w-24 h-24 bg-yellow-500 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-2000 z-0"></div>
          <div class="absolute bottom-1/4 left-1/3 w-24 h-24 bg-yellow-700 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-4000 z-0"></div>
        </section>

        <form on:submit|preventDefault={handleSubmit} class="space-y-10 animate-fade">
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

          <div class="space-y-5">
            <label for="amount" class="block text-xl font-medium text-gray-300">
              Amount (USD)
            </label>

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

          <button
            type="submit"
            class="w-full px-10 py-5 text-black text-xl font-bold rounded-lg focus:outline-none focus:ring-2 focus:ring-yellow-500 transition-colors group shadow-lg hover:cursor-pointer flex items-center justify-center"
            style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);"
          >
            <span>Donate Now</span>
            <span class="inline-block transition-transform group-hover:translate-x-1 ml-3 text-2xl">→</span>
          </button>

          {#if showError && Object.values(formErrors).some(Boolean)}
            <p class="text-center text-yellow-400 text-lg">
              Please fill in all required fields correctly.
            </p>
          {/if}
        </form>

        <div class="mt-16 animate-fade-down animate-delay-300">
          <button
            on:click={() => showSponsorshipPackage = !showSponsorshipPackage}
            class="w-full flex items-center justify-between px-6 py-4 bg-[#0f0e13] border border-white/20 rounded-lg text-xl text-white hover:bg-white/10 transition-colors hover:cursor-pointer"
          >
            <span class="font-semibold">Sponsorship Packages</span>
            <svg 
              class="w-6 h-6 transform transition-transform {showSponsorshipPackage ? 'rotate-180' : ''}" 
              fill="none" 
              stroke="currentColor" 
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          
          {#if showSponsorshipPackage}
            <div class="mt-4 rounded-lg overflow-hidden border border-white/20 shadow-2xl">
              <img 
                src={SponsorshipPackage} 
                alt="Undefined Robotics Sponsorship Packages details, listing tiers and benefits." 
                class="w-full h-auto"
              />
            </div>
          {/if}
        </div>
    </div>
  </div>
</main>