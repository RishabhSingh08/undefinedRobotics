<script>
  // Dummy robot component images
  import robotMainImage from "../../lib/images/robot/image.png";
  import robotPart1 from "../../lib/images/robot/part1.png";
  import robotPart2 from "../../lib/images/robot/part2.png";
  import robotPart3 from "../../lib/images/robot/part3.png";
</script>

<svelte:head>
  <title>Undefined Robotics | Robots</title>
  <meta name="description" content="Meet InfiNemo: The Undefined Robotics (Team #25782) competition robot for the FTC Into The Deep season. Featuring a custom chassis, 3-DOF claw intake, and autonomous navigation." />
  <meta name="keywords" content="FTC Robot, Into The Deep, InfiNemo, Undefined Robotics, Team 25782, Robotics Engineering, Mecanum Chassis, Linear Slides, Autonomous Robot" />

  <link rel="canonical" href="https://undefinedrobotics.org/robot" />

  <meta property="og:title" content="InfiNemo | High-Performance FTC Robot" />
  <meta property="og:description" content="Explore the engineering behind our 2025 competition robot: Custom machining, 3D printed intake, and advanced odometry." />
  <meta property="og:image" content="https://undefinedrobotics.org/robot-og.png" /> <meta property="og:url" content="https://undefinedrobotics.org/robot" />
  <meta property="og:type" content="article" />

  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="InfiNemo: FTC Into The Deep Robot Reveal" />
  <meta name="twitter:description" content="Undefined Robotics #25782 presents InfiNemo. Multi-modular design with rapid cycling capabilities." />
  <meta name="twitter:image" content="https://undefinedrobotics.org/robot-og.png" />

  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Product",
    "name": "InfiNemo FTC Robot",
    "image": "https://undefinedrobotics.org/robot-main.png",
    "description": "Autonomous competition robot designed for FIRST Tech Challenge Into The Deep season.",
    "brand": {
      "@type": "Organization",
      "name": "Undefined Robotics"
    },
    "manufacturer": {
      "@type": "Organization",
      "name": "Undefined Robotics Team #25782"
    },
    "category": "Robotics"
  }
  </script>
</svelte:head>

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

  <section class="relative z-10 px-4 ">
    <div class="max-w-7xl mx-auto text-center animate-fade-down">
      <h1 class="text-4xl md:text-6xl font-semibold mb-8 ">
        InfiNemo
      </h1>
      <p class="text-lg md:text-xl text-gray-400 max-w-3xl mx-auto">
        Meet our robot designed for the FTC "INTO THE DEEP" 24-25 season
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
        <div class="flex items-center justify-center animate-fade-right">
          <img src={robotMainImage} alt="InfiNemo FTC Competition Robot Main View" class="w-xl h-xl object-cover" />
        </div>
      </div>
      <div class="space-y-6">
        <div class=" p-6 animate-fade-left">
          <div class="">
            <div class="inline-block text-gray-900 py-3 px-6 rounded-lg font-bold text-2xl mb-4" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              #25782 Undefined
            </div>
          </div>

          <p class="text-xl">Features a multi-modular design focused on adaptability, utilizing a rotating linear extension arm paired with a 3-DOF claw intake for efficient sample collection. In the autonomous period, it can consistently deliver 5 samples or 4 specimens using various control strategies (odo pods + limelight). During tele-op period (controller), it can place up to 15 samples in bucket thru rapid cycling and parks during endgame.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="flex flex-col items-center animate-fade-up">
    <div class="w-4 h-4 bg-white rounded-full border-2 border-gray-300"></div>
    <div class="w-0.5 h-32 bg-gray-300"></div>
</div>

<section class="relative z-10 px-4 pb-16 animate-fade-up">
  <div class="max-w-7xl mx-auto relative">
    <div class="hidden md:block absolute top-1/2 left-0 right-0 h-0.5 bg-gray-300 transform -translate-y-1/2 z-0"></div>
    
    <div class="md:hidden absolute top-0 bottom-0 left-1/2 w-0.5 bg-gray-300 transform -translate-x-1/2 z-0"></div>
    
    <div class="grid md:grid-cols-3 gap-8 relative z-10">
      <div class="bg-[#20242c] backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-[#2A2F34] transition-all duration-300">
        <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
          <img src={robotPart1} alt="3-DOF Intake Mechanism with Axon Minis" class="w-full h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold text-white mb-3">Intake Mechanism</h3>
        <p class="text-gray-300">3D modeled (Fusion 360) and printed Intake griper with 3 degrees of freedom powered by Axon minis with sequential programming enhancements and feedback control loops.</p>
      </div>
      
      <div class="bg-[#20242c] backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-[#2A2F34] transition-all duration-300">
        <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
          <img src={robotPart2} alt="Custom Aluminum Machined Chassis with Mecanum Wheels" class="w-full h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold text-white mb-3">Custom Chassis</h3>
        <p class="text-gray-300">Custom aluminum machined parallel structure chassis with pentagonal pocketing boasting new grippy mecanum wheels for responsive omnidirectional movement powered by quad-motor setup.</p>
      </div>
      
      <div class="bg-[#20242c] backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-[#2A2F34] transition-all duration-300">
        <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
          <img src={robotPart3} alt="Misumi Linear Slide Scoring Arm" class="w-full h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold text-white mb-3">Scoring Arm</h3>
        <p class="text-gray-300">Misumi linear slides with single motor control featuring custom 3D printed inserts and nylon coated continuous double spool stringing with counter-spring retraction for smooth linear extension.</p>
      </div>
    </div>
  </div>
  
</section>

<div class="relative z-10 px-4 animate-fade">
  <div class="max-w-7xl mx-auto text-center">
    <a
      href="https://www.missingamps.team"
      target="_blank"
      rel="noopener noreferrer"
      class="inline-block bg-purple-600 hover:bg-purple-700 text-white font-semibold py-3 px-6 rounded-xl shadow-lg transition duration-300"
    >
      View Missing Amps Robot
      <span>
        <i class="fa-solid fa-up-right-from-square"></i>
      </span>
    </a>
  </div>
</div>

</main>