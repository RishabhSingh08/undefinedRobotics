<script>
  // Dummy robot component images
    

  import robotMainImage from "../../lib/images/robot/image2.png";
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
        Our Robot
      </h1>
      <p class="text-lg md:text-xl text-gray-400 max-w-3xl mx-auto">
        Meet our competition robot designed for the FIRST Tech Challenge "INTO THE DEEP" season
      </p>
    </div>
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
          <h3 class="text-3xl font-bold  mb-4">2024 - 2025 Season</h3>
          <p class="text-xl">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem tempore libero explicabo nostrum in, voluptatem error provident voluptate ut voluptatum! Eveniet reiciendis minus veritatis voluptates unde placeat voluptate hic doloremque maiores eaque temporibus, veniam est pariatur, corrupti iure aperiam eos cum quam. Delectus, optio asperiores.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="flex flex-col items-center">
    <div class="w-4 h-4 bg-white rounded-full border-2 border-gray-300"></div>
    <div class="w-0.5 h-96 bg-gray-300"></div>
</div>

  <section class="relative z-10 px-4 pb-16">
    <div class="max-w-7xl mx-auto">
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



</main>