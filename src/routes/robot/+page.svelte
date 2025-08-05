<script>
  // Dummy robot component images
    

  import robotMainImage from "../../lib/images/robot/image.png";
  import robotPart1 from "../../lib/images/robot/part1.png";
  import robotPart2 from "../../lib/images/robot/part2.png";
  import robotPart3 from "../../lib/images/robot/part3.png";
</script>

<style>
  .cedarville-cursive-regular {
    font-family: "Cedarville Cursive", cursive;
    font-weight: 400;
    font-style: normal;
  }

  @keyframes blob {
    0% {
      transform: translate(0px, 0px) scale(1);
    }
    33% {
      transform: translate(30px, -50px) scale(1.1);
    }
    66% {
      transform: translate(-20px, 20px) scale(0.9);
    }
    100% {
      transform: translate(0px, 0px) scale(1);
    }
  }

  .animate-blob {
    animation: blob 7s infinite;
  }

  .animation-delay-2000 {
    animation-delay: 2s;
  }

  .animation-delay-4000 {
    animation-delay: 4s;
  }
</style>

<main class="text-white overflow-hidden relative dm-sans py-32 min-h-screen">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <!-- Hero Section with Season Info -->
  <section class="relative z-10 px-4 ">
    <div class="max-w-7xl mx-auto text-center">
      <h1 class="text-4xl md:text-6xl font-semibold mb-8">
        Infinemo
      </h1>
      <p class="text-lg md:text-xl text-gray-400 max-w-3xl mx-auto">
        Meet our competition robot designed for the FTC "INTO THE DEEP" season
      </p>
    </div>
      <div class="absolute top-1/4 left-10 w-24 h-24 bg-yellow-200 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob z-0"></div>
  <div class="absolute top-1/3 right-10 w-24 h-24 bg-yellow-500 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-2000 z-0"></div>
  <div class="absolute bottom-1/4 left-1/3 w-24 h-24 bg-yellow-700 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-4000 z-0"></div>

  </section>

<section class="relative z-10 px-4 pt-16 ">
  <div class="max-w-7xl mx-auto ">
    <div class="grid lg:grid-cols-2 items-center">
      <div class="lg:col-span-1">
        <div class="flex items-center justify-center">
          <img src={robotMainImage} alt="Competition Robot" class="w-xl h-xl object-cover" />
        </div>
      </div>
      <div class="space-y-6">
        <div class=" p-6 ">
          <div class="">
            <div class="inline-block bg-yellow-400 text-gray-900 py-3 px-6 rounded-lg font-bold text-2xl mb-4">
              2024 - 2025 Season
            </div>
          </div>

          <p class="text-xl">Features a multi-modular design focused on adaptability, utilizing a rotating linear extension arm paired with a 3-DOF claw intake for efficient sample collection. In the autonomous period, it can consistently deliver 5 samples or 4 specimens using various control strategies (odo pods + limelight). During tele-op period (controller), it can place up to 15 samples in bucket thru rapid cycling and parks during endgame.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="flex flex-col items-center">
    <div class="w-4 h-4 bg-white rounded-full border-2 border-gray-300"></div>
    <div class="w-0.5 h-32 bg-gray-300"></div>
</div>

<section class="relative z-10 px-4 pb-16">
  <div class="max-w-7xl mx-auto relative">
    <div class="absolute top-1/2 left-0 right-0 h-0.5 bg-gray-300 transform -translate-y-1/2 z-0"></div>
    
    <div class="grid md:grid-cols-3 gap-8 relative z-10">
      <div class="bg-[#20242c] backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-[#2A2F34] transition-all duration-300">
        <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
          <img src={robotPart1} alt="Drive System Component" class="w-full h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold text-white mb-3">Custom Chassis</h3>
        <p class="text-gray-300">Custom aluminum machined parallel structure chassis with pentagonal pocketing boasting new grippy mecanum wheels for responsive omnidirectional movement powered by quad-motor setup.</p>
      </div>
      
      <div class="bg-[#20242c] backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-[#2A2F34] transition-all duration-300">
        <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
          <img src={robotPart2} alt="Intake Mechanism Component" class="w-full h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold text-white mb-3">Intake Mechanism</h3>
        <p class="text-gray-300">3D modeled (Fusion 360) and printed Intake griper with 3 degrees of freedom powered by Axon minis with sequential programming enhancements and feedback control loops.</p>
      </div>
      
      <div class="bg-[#20242c] backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-[#2A2F34] transition-all duration-300">
        <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
          <img src={robotPart3} alt="Scoring Arm Component" class="w-full h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold text-white mb-3">Scoring Arm</h3>
        <p class="text-gray-300">Misumi linear slides with single motor control featuring custom 3D printed inserts and nylon coated continuous double spool stringing with counter-spring retraction for smooth linear extension.</p>
      </div>
    </div>
  </div>
  
</section>

<!-- Redirect Button -->
<div class="relative z-10 px-4">
  <div class="max-w-7xl mx-auto text-center">
    <a
      href="https://www.missingamps.team"
      target="_blank"
      rel="noopener noreferrer"
      class="inline-block bg-purple-600 hover:bg-purple-700 text-white font-semibold py-3 px-6 rounded-xl shadow-lg transition duration-300"
    >
      View Missing Amps Robot
      <span>
<i class="fa-solid fa-up-right-from-square"></i>      </span>
    </a>
  </div>
</div>

</main>