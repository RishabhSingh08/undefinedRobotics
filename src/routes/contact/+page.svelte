<script>
    import IconLogo from "../../lib/images/logo.png";
    import { onMount } from 'svelte';
    import emailjs from '@emailjs/browser';

    let formData = {
        name: '',
        email: '',
        company: '',
        message: '',
    };

    let submitStatus = ''; // Track form submission status


    const contactInfo = {
        email: 'contact@undefinedrobotics.org',
        phone: "(469) 819-7461",
        location: 'Plano, Texas',
        availability: 'Monday - Friday: 9:00 AM - 9:00 PM CST',
        response: 'We typically respond within 24 hours'
    };

    async function handleSubmit() {
        submitStatus = 'Sending...';

        const templateParams = {
            name: formData.name,
            email: formData.email,
            company: formData.company,
            message: formData.message,
        };

        try {
            const response = await emailjs.send(
                'service_ilqucba',
                'template_sxyicx8',
                templateParams,
                'zpT2fUZ-MqVc6ARfz'
            );
            submitStatus = 'Sent!';
            
            // Reset form after successful submission
            formData = {
                name: '',
                email: '',
                company: '',
                message: '',
            };

            // Clear success message after 3 seconds
            setTimeout(() => {
                submitStatus = '';
            }, 3000);

        } catch (error) {
            console.error('FAILED...', error);
            submitStatus = 'Failed to send. Please try again.';
            
            // Clear error message after 3 seconds
            setTimeout(() => {
                submitStatus = '';
            }, 3000);
        }
    }
</script>

<main id="record" class="px-4 py-32 relative z-10 min-h-screen">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <div class="max-w-5xl mx-auto">
    
    <div class="text-center mb-16">
      <h1 class="text-4xl md:text-6xl font-semibold text-white mb-6">
        Contact
      </h1>
      <p class="text-lg md:text-2xl text-gray-200 max-w-2xl mx-auto leading-relaxed">
        Have questions? Interested in a position? Want to become a sponsor? Get it touch!
      </p>
    </div>

            <div class="max-w-7xl mx-auto px-4">
            <div class="grid md:grid-cols-2 gap-16 ">
                <!-- Contact Information -->
                <div class="space-y-12 motion-duration-2000 motion-preset-slide-right-lg">
                    <div>
                        <h2 class="text-3xl font-bold mb-8">Contact Information</h2>
                        <div class="space-y-6">
                            <div class="flex items-center space-x-4">
                                <span class="text-2xl">📧</span>
                                <div>
                                    <p class="font-semibold">Email</p>
                                    <a href="mailto:Stryng.dev@gmail.com" class="text-gray-400 hover:text-white transition-colors">
                                        {contactInfo.email}
                                    </a>
                                </div>
                            </div>
                            <div class="flex items-center space-x-4">
                                <span class="text-2xl">📱</span>
                                <div>
                                    <p class="font-semibold">Phone</p>
                                    <a href="tel:9726969564" class="text-gray-400 hover:text-white transition-colors">
                                        {contactInfo.phone}
                                    </a>
                                </div>
                            </div>
                            <div class="flex items-center space-x-4">
                                <span class="text-2xl">📍</span>
                                <div>
                                    <p class="font-semibold">Location</p>
                                    <p class="text-gray-400">{contactInfo.location}</p>
                                </div>
                            </div>
                        </div>
                    </div>


                  <div>
                    <h3 class="text-2xl font-bold mb-4">Send us a Friend Request</h3>
                    <div class="flex items-center space-x-4">
                      <span class="text-2xl">        <svg class="w-5 h-5 text-[#5865F2]" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M20.317 4.369a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.078.037c-.21.375-.444.864-.608 1.25a18.518 18.518 0 0 0-5.432 0 12.51 12.51 0 0 0-.619-1.25.077.077 0 0 0-.078-.037A19.736 19.736 0 0 0 3.677 4.369a.069.069 0 0 0-.032.027C.533 9.14-.32 13.694.099 18.184a.082.082 0 0 0 .031.056 19.952 19.952 0 0 0 5.993 3.045.077.077 0 0 0 .084-.027c.461-.63.873-1.295 1.226-1.993a.076.076 0 0 0-.041-.103 13.183 13.183 0 0 1-1.872-.89.078.078 0 0 1-.008-.13c.126-.095.252-.19.373-.29a.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.076.076 0 0 1 .078.009c.12.1.246.195.372.29a.078.078 0 0 1-.006.13 12.442 12.442 0 0 1-1.873.889.075.075 0 0 0-.04.104c.36.698.772 1.362 1.225 1.993a.077.077 0 0 0 .084.027 19.908 19.908 0 0 0 6.001-3.045.078.078 0 0 0 .03-.055c.5-5.177-.838-9.701-3.59-13.788a.062.062 0 0 0-.03-.028zM8.02 15.331c-1.183 0-2.157-1.085-2.157-2.419 0-1.333.955-2.418 2.157-2.418 1.21 0 2.174 1.094 2.157 2.418 0 1.334-.955 2.42-2.157 2.42zm7.938 0c-1.183 0-2.157-1.085-2.157-2.419 0-1.333.954-2.418 2.157-2.418 1.21 0 2.174 1.094 2.157 2.418 0 1.334-.947 2.42-2.157 2.42z"/>
                          </svg></span>
                      <div>
                        <div class="inline-flex items-center bg-gray-800 text-gray-300 px-3 py-1 rounded-full space-x-2">

                          <span class="">undefinedrobotics</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- Contact Form -->
                <div class="bg-gray-800/50 backdrop-blur-lg border border-gray-700 p-8 rounded-xl motion-duration-2000 motion-preset-slide-left-lg">
                    <form on:submit|preventDefault={handleSubmit} class="space-y-6" method="POST">


                        <div class="grid md:grid-cols-2 gap-6">
                            
                            <div>
                                <label for="name" class="block text-sm font-medium mb-2">Name</label>
                                <input
                                    type="text"
                                    id="name"
                                    bind:value={formData.name}
                                    class="w-full px-4 py-2 bg-gray-900 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"
                                    required
                                />
                            </div>
                            
                            <div>
                                <label for="email" class="block text-sm font-medium mb-2">Email</label>
                                <input
                                    type="email"
                                    id="email"
                                    bind:value={formData.email}
                                    class="w-full px-4 py-2 bg-gray-900 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"
                                    required
                                />
                            </div>
                        </div>

                        <div>
                            <label for="company" class="block text-sm font-medium mb-2">Company</label>
                            <input
                                type="text"
                                id="company"
                                bind:value={formData.company}
                                class="w-full px-4 py-2 bg-gray-900 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"
                                required
                            />
                        </div>


                        <div>
                            <label for="message" class="block text-sm font-medium mb-2">Message</label>
                            <textarea
                                id="message"
                                bind:value={formData.message}
                                rows="5"
                                class="w-full px-4 py-2 bg-gray-900 border border-gray-700 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"
                                required
                            ></textarea>
                        </div>

                        <div class="flex flex-col items-center space-y-4">
                            <button
                                type="submit"
                                class="w-full bg-white text-black px-8 py-4 rounded-full text-lg font-semibold hover:bg-gray-200 transition-colors disabled:opacity-50 disabled:cursor-not-allowed"
                                disabled={submitStatus === 'Sending...'}
                            >
                                Send Message
                            </button>
                            
                            {#if submitStatus}
                                <p class="text-center {submitStatus === 'Sent!' ? 'text-green-400' : submitStatus === 'Sending...' ? 'text-blue-400' : 'text-red-400'}">
                                    {submitStatus}
                                </p>
                            {/if}
                        </div>
                    </form>
                </div>
            </div>
        </div>


  </div>
</main>

<style>
</style>


