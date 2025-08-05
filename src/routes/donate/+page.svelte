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
  :global(body) {
    background: #333030;
    min-height: 100vh;
    margin: 0;
  }
</style>

<main class="rounded-3xl pt-32 pb-16 min-h-screen flex items-center justify-center" style="background: #000;">
  <div class="max-w-lg mx-auto bg-white rounded-xl shadow-lg p-6 space-y-8">
    <div class="text-center space-y-4">
      {#if IconLogo}
        <img src={IconLogo} alt="Organization Logo" class="h-24 mx-auto" />
      {/if}
      <h2 class="text-3xl font-bold text-gray-900">Make a Donation</h2>
      <p class="text-gray-600">
        Your generous contributions help us make a global impact. Join us in building a brighter future.
      </p>
    </div>
    <form on:submit={handleSubmit} class="space-y-6">
      <div class="space-y-1">
        <label for="name" class="block text-sm font-medium text-gray-700">Name*</label>
        <input
          id="name"
          type="text"
          bind:value={name}
          class="w-full px-4 py-2 rounded-lg border focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none {formErrors.name ? 'border-yellow-500' : 'border-gray-300'}"
          placeholder="Your Name"
        />
        {#if formErrors.name && showError}
          <p class="text-yellow-600 text-sm">{formErrors.name}</p>
        {/if}
      </div>
      <div class="space-y-1">
        <label for="email" class="block text-sm font-medium text-gray-700">Email*</label>
        <input
          id="email"
          type="email"
          bind:value={email}
          class="w-full px-4 py-2 rounded-lg border focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none {formErrors.email ? 'border-yellow-500' : 'border-gray-300'}"
          placeholder="Your Email"
        />
        {#if formErrors.email && showError}
          <p class="text-yellow-600 text-sm">{formErrors.email}</p>
        {/if}
      </div>
      <div class="space-y-1">
        <label for="amount" class="block text-sm font-medium text-gray-700">Amount (USD)*</label>
        <input
          id="amount"
          type="number"
          bind:value={amount}
          min="0"
          step="0.01"
          class="w-full px-4 py-2 rounded-lg border focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500 outline-none {formErrors.amount ? 'border-yellow-500' : 'border-gray-300'}"
          placeholder="Enter Amount"
        />
        {#if formErrors.amount && showError}
          <p class="text-yellow-600 text-sm">{formErrors.amount}</p>
        {/if}
      </div>
      <button
        type="submit"
        class="w-full px-6 py-3 text-white bg-yellow-500 rounded-lg hover:bg-yellow-600 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-yellow-500 transition-colors duration-200"
      >
        Donate Now
      </button>
      {#if showError && Object.values(formErrors).some(Boolean)}
        <p class="text-center text-yellow-600 font-medium">Please fill in all required fields correctly</p>
      {/if}
    </form>
  </div>
</main>