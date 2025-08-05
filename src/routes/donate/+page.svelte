// import IconLogo from "../../lib/images/logo.png";




<main class="relative min-h-screen flex items-center justify-center bg-black py-20 px-2 overflow-x-hidden">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.08)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>
  <div class="relative z-10 w-full max-w-6xl mx-auto">
    <div class="flex flex-col md:flex-row gap-8 md:gap-12 items-center justify-center">
      <!-- Left: Info Block (mirrored) -->
      <div class="bg-white/10 backdrop-blur-lg rounded-3xl shadow-2xl p-8 md:p-12 flex flex-col items-center border border-white/20 w-full md:w-1/2 order-2 md:order-1">
        <h1 class="text-4xl md:text-5xl font-extrabold text-yellow-400 mb-4 drop-shadow-lg tracking-tight text-center">Why Donate?</h1>
        <ul class="text-lg md:text-xl text-gray-100 mb-6 space-y-3 max-w-md mx-auto list-disc list-inside">
          <li><span class="text-yellow-300 font-bold">Expand STEM access</span> for underrepresented youth</li>
          <li>Fund <span class="text-yellow-300 font-bold">robotics kits & outreach</span> in our community</li>
          <li>Support <span class="text-yellow-300 font-bold">competition travel</span> and team growth</li>
          <li>All donations are <span class="text-yellow-300 font-bold">tax-deductible</span> via Hack Club</li>
        </ul>
        <p class="text-base md:text-lg text-gray-300 text-center">Thank you for supporting <span class="text-yellow-300 font-bold">Undefined Robotics</span>!</p>
      </div>
      <!-- Right: Donation Iframe Block -->
      <div class="bg-white/10 backdrop-blur-lg rounded-3xl shadow-2xl p-8 md:p-12 flex flex-col items-center border border-white/20 w-full md:w-1/2 order-1 md:order-2">
        <h2 class="text-3xl md:text-4xl font-bold text-yellow-300 mb-4 text-center">Donate Now</h2>
        <div class="w-full max-w-xl min-h-[600px] flex items-center justify-center bg-[#18181b] border border-[#23234b] rounded-2xl shadow-lg overflow-hidden">
          <iframe 
            src="https://hcb.hackclub.com/donations/start/undefined-robotics" 
            style="background: transparent;" 
            name="donateFrame" 
            scrolling="yes" 
            frameborder="0" 
            marginheight="0px" 
            marginwidth="0px" 
            height="600px" 
            width="100%" 
            allowfullscreen 
            title="Donate to Undefined Robotics via Hack Club"
            class="w-full min-h-[600px]"
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</main>

<style>
</style>
