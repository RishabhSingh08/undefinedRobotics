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
  <section class="relative z-10 px-4">
    <div class="max-w-7xl mx-auto text-center">
      <h1 class="text-4xl md:text-6xl font-semibold mb-8">
        Our Robot
      </h1>
      <p class="text-lg md:text-xl text-gray-400 max-w-3xl mx-auto">
        Meet our competition robot designed for the FIRST Tech Challenge "INTO THE DEEP" season
      </p>
    </div>
  </section>

  <section class="relative z-10 px-4 py-16">
    <div class="max-w-7xl mx-auto">
      <div class="grid lg:grid-cols-3 gap-8">
        <div class="lg:col-span-2">
          <div class="bg-gray-300 rounded-xl aspect-video flex items-center justify-center border border-gray-400 overflow-hidden">
            <img src={robotMainImage} alt="Competition Robot" class="w-full h-full object-cover" />
          </div>
        </div>

        <div class="space-y-6">
          <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20">
            <h3 class="text-xl font-bold text-yellow-300 mb-4">Robot Specifications</h3>
            <div class="space-y-3 text-gray-300">
              <div class="flex justify-between">
                <span>Height:</span>
                <span class="text-white">X inches</span>
              </div>
              <div class="flex justify-between">
                <span>Width:</span>
                <span class="text-white">X inches</span>
              </div>
              <div class="flex justify-between">
                <span>Length:</span>
                <span class="text-white">X inches</span>
              </div>
              <div class="flex justify-between">
                <span>Weight:</span>
                <span class="text-white">X lbs</span>
              </div>
              <div class="flex justify-between">
                <span>Drive Type:</span>
                <span class="text-white">X</span>
              </div>
            </div>
          </div>

          <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20">
            <h3 class="text-xl font-bold text-green-300 mb-4">Key Features</h3>
            <div class="space-y-3">
              <div class="flex items-start">
                <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                <span class="text-gray-300 text-sm">some words here</span>
              </div>
              <div class="flex items-start">
                <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                <span class="text-gray-300 text-sm">some words here</span>
              </div>
              <div class="flex items-start">
                <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                <span class="text-gray-300 text-sm">some words here</span>
              </div>
              <div class="flex items-start">
                <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
                <span class="text-gray-300 text-sm">some words here</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="relative z-10 px-4 py-16">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-5xl font-semibold text-center text-gray-100 tracking-tight mb-16">
        Robot Components
      </h2>
      
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
            <img src={robotPart1} alt="Drive System Component" class="w-full h-full object-cover" />
          </div>
          <h3 class="text-xl font-bold text-white mb-3">Drive System</h3>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Pariatur consectetur quisquam veniam natus fugit, accusantium nesciunt dicta aut incidunt cumque hic, aliquam, inventore qui illum.</p>

        </div>

        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
            <img src={robotPart2} alt="Intake Mechanism Component" class="w-full h-full object-cover" />
          </div>
          <h3 class="text-xl font-bold text-white mb-3">Intake Mechanism</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias tempore, nostrum repellat laudantium recusandae illum voluptatum aliquam veniam et illo quidem nulla. Aliquam, at molestiae.</p>

        </div>

        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <div class="bg-gray-300 rounded-lg aspect-square mb-6 flex items-center justify-center border border-gray-400 overflow-hidden">
            <img src={robotPart3} alt="Scoring Arm Component" class="w-full h-full object-cover" />
          </div>
          <h3 class="text-xl font-bold text-white mb-3">Scoring Arm</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tenetur, excepturi quaerat. Unde dolorum saepe, iusto ut nulla suscipit fugiat inventore et, recusandae laudantium deserunt ratione!</p>

        </div>
      </div>
    </div>
  </section>

  <section class="relative z-10 px-4 py-16">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-5xl font-semibold text-center text-gray-100 tracking-tight mb-16">
        Performance Statistics
      </h2>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 text-center hover:bg-white/15 transition-all duration-300">
          <div class="text-3xl font-bold text-yellow-400 mb-2">X%</div>
          <div class="text-gray-300">Statistic 1</div>
        </div>
        
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 text-center hover:bg-white/15 transition-all duration-300">
          <div class="text-3xl font-bold text-green-400 mb-2">X</div>
          <div class="text-gray-300">Statistic 2</div>
        </div>
        
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 text-center hover:bg-white/15 transition-all duration-300">
          <div class="text-3xl font-bold text-blue-400 mb-2">X</div>
          <div class="text-gray-300">Statistic 3</div>
        </div>
        
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20 text-center hover:bg-white/15 transition-all duration-300">
          <div class="text-3xl font-bold text-purple-400 mb-2">X%</div>
          <div class="text-gray-300">Statistic 4</div>
        </div>
      </div>
    </div>
  </section>


</main>