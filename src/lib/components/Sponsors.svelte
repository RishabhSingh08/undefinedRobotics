<script>
  import { onMount } from 'svelte';
  
  import s from "../images/sponsors/s.png";
  import s1 from "../images/sponsors/s1.png";
  import s2 from "../images/sponsors/s2.png";
  import s3 from "../images/sponsors/s3.png";
  import s4 from "../images/sponsors/s4.png";
  import s5 from "../images/sponsors/s5.png";
  import s6 from "../images/sponsors/s6.png";
  import s7 from "../images/sponsors/s7.png";
  import s8 from "../images/sponsors/s8.png";
  import s9 from "../images/sponsors/s9.png";
  import s10 from "../images/sponsors/s10.png";
  import s11 from "../images/sponsors/s11.png";
  import s12 from "../images/sponsors/s12.png";
  import fabworks from "../images/fabworks.png";

  const platinumSponsors = [
    { src: s10, href: 'https://buildshowlive.com/', name: 'Build Show' },
    { src: s7, href: 'https://www.solaceglobal.world/', name: 'Solace Global' },
    { src: s11, href: 'https://ghaasfoundation.org/', name: 'Gene Haas' },
  ];

  const goldSponsors = [
    { src: s9, href: 'https://www.mmmfg.com/', name: 'M&M' },
    { src: s2, href: 'https://polymaker.com/', name: 'Polymaker' },
    { src: s3, href: 'https://www.twc.texas.gov/', name: 'TWC Commission' }
  ];

  const silverSponsors = [
    { src: s12, href: 'https://www.firstinspires.org/', name: 'FIRST Robotics' },
    { src: s8, href: 'https://svtronics.com/', name: 'SV Tronics' },
    { src: s5, href: 'https://www.bosch.com/', name: 'Bosch' },
    { src: s6, href: 'https://www.jabil.com/', name: 'Jabil' },
    { src: fabworks, href: 'https://www.fabworks.com/', name: 'Fabworks' }
  ];

  const carouselSponsors = [
    ...goldSponsors.map(sponsor => ({ ...sponsor, tier: 'GOLD' })),
    ...silverSponsors.map(sponsor => ({ ...sponsor, tier: 'SILVER' }))
  ];

  const duplicatedSponsors = [...carouselSponsors, ...carouselSponsors];

  let platinumRefs = [];
  
  onMount(() => {
    platinumRefs.forEach((ref, index) => {
      if (ref) ref.style.animationDelay = `${index * 0.2}s`;
    });
  });
</script>

<style>
  .cedarville-cursive-regular {
    font-family: "Cedarville Cursive", cursive;
    font-weight: 400;
    font-style: normal;
  }

  @keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
  @keyframes float { 0%, 100% { transform: translateY(0px); } 50% { transform: translateY(-10px); } }
  .platinum-float { animation: float 3s ease-in-out infinite; }
  @keyframes shimmer { 0% { background-position: -1000px 0; } 100% { background-position: 1000px 0; } }
  .platinum-shimmer { background: linear-gradient(90deg, transparent 0%, rgba(255,255,255,0.1) 50%, transparent 100%); background-size: 1000px 100%; animation: shimmer 3s infinite; }

  @media (min-width: 768px) {
    .desktop-carousel-track {
      width: max-content;
      animation: scroll 30s linear infinite;
    }
    .desktop-carousel-track:hover { animation-play-state: paused; }

    /* Grayscale images on desktop only */
    .grayscale-container img {
      filter: grayscale(100%);
      transition: filter 0.3s ease, transform 0.3s ease;
    }

    .grayscale-container:hover img {
      filter: grayscale(0%);
    }
  }
</style>

<div>
  <h2 class="text-3xl sm:text-5xl md:text-7xl text-center text-white mt-20 sm:mt-32 mb-16 sm:mb-24 px-4 cedarville-cursive-regular animate-fade">
    Thank You to Our Sponsors and Partners!
  </h2>

  <section class="w-full relative z-10 mb-20 px-4 animate-fade">
    <div class="max-w-7xl mx-auto">
      <h3 class="text-2xl sm:text-3xl md:text-5xl font-bold text-center mb-8 sm:mb-12 bg-gradient-to-r from-purple-400 via-pink-400 to-purple-400 bg-clip-text text-transparent ">
        Platinum Sponsors
      </h3>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 sm:gap-8 lg:gap-12">
        {#each platinumSponsors as sponsor, index}
          <a href={sponsor.href} target="_blank" rel="noopener noreferrer" bind:this={platinumRefs[index]} class="group relative platinum-float grayscale-container">
            <div class="relative overflow-hidden rounded-2xl bg-gradient-to-br from-purple-600/20 to-pink-600/20 p-1 transition-all duration-300 hover:scale-105">
              <div class="platinum-shimmer absolute inset-0 rounded-2xl"></div>
              <div class="relative bg-gray-900/90 backdrop-blur-sm rounded-xl p-6 sm:p-8 border border-purple-500/30">
                <div class="flex items-center justify-center h-24 sm:h-32 md:h-40">
                  <img src={sponsor.src} alt={sponsor.name} class="max-h-full max-w-full object-contain transition-all duration-300" />
                </div>
                <div class="mt-4 text-center">
                  <p class="text-purple-300 font-semibold text-base sm:text-lg">{sponsor.name}</p>
                </div>
              </div>
            </div>
          </a>
        {/each}
      </div>
    </div>
  </section>

  <section class="w-full relative z-10 pb-20 sm:pb-32 md:overflow-hidden animate-fade">
    <div class="max-w-7xl mx-auto px-4 mb-6 sm:mb-8">
      <h3 class="text-xl sm:text-2xl md:text-4xl font-bold text-center bg-gradient-to-r from-yellow-400 via-gray-300 to-yellow-400 bg-clip-text text-transparent">
        Gold & Silver Sponsors
      </h3>
    </div>

    <div class="relative">
      <div class="absolute left-0 top-0 bottom-0 w-16 sm:w-32 bg-gradient-to-r from-gray-900 to-transparent z-10 hidden md:block"></div>
      <div class="absolute right-0 top-0 bottom-0 w-16 sm:w-32 bg-gradient-to-l from-gray-900 to-transparent z-10 hidden md:block"></div>
      
      <div class="flex flex-wrap justify-center gap-4 sm:gap-6 px-4 md:hidden">
        {#each carouselSponsors as sponsor}
          <a href={sponsor.href} target="_blank" rel="noopener noreferrer" class="flex-shrink-0 group relative">
            <div class="relative bg-gray-800/50 backdrop-blur-sm rounded-xl p-4 sm:p-6 border border-gray-700 transition-all duration-300 hover:scale-105 hover:border-gray-500">
              <div class="absolute -top-2 -left-2 sm:-top-3 sm:-left-3 z-20">
                <span class={`px-2 py-1 text-xs font-bold rounded-full ${sponsor.tier === 'GOLD' ? 'bg-gradient-to-r from-yellow-400 to-yellow-600 text-yellow-900' : 'bg-gradient-to-r from-gray-300 to-gray-500 text-gray-900'}`}>
                  {sponsor.tier}
                </span>
              </div>
              <div class="flex items-center justify-center w-32 h-20 sm:w-40 sm:h-24 md:w-48 md:h-28">
                <img src={sponsor.src} alt={sponsor.name} class="max-h-full max-w-full object-contain opacity-80 group-hover:opacity-100 transition-opacity duration-300" />
              </div>
            </div>
          </a>
        {/each}
      </div>

      <div class="hidden md:flex md:flex-nowrap md:justify-start desktop-carousel-track">
        {#each duplicatedSponsors as sponsor}
          <a href={sponsor.href} target="_blank" rel="noopener noreferrer" class="flex-shrink-0 group relative mx-4 sm:mx-6 grayscale-container">
            <div class="relative bg-gray-800/50 backdrop-blur-sm rounded-xl p-4 sm:p-6 border border-gray-700 transition-all duration-300 hover:scale-105 hover:border-gray-500">
              <div class="absolute -top-2 -left-2 sm:-top-3 sm:-left-3 z-20">
                <span class={`px-2 py-1 text-xs font-bold rounded-full ${sponsor.tier === 'GOLD' ? 'bg-gradient-to-r from-yellow-400 to-yellow-600 text-yellow-900' : 'bg-gradient-to-r from-gray-300 to-gray-500 text-gray-900'}`}>
                  {sponsor.tier}
                </span>
              </div>
              <div class="flex items-center justify-center w-32 h-20 sm:w-40 sm:h-24 md:w-48 md:h-28">
                <img src={sponsor.src} alt={sponsor.name} class="max-h-full max-w-full object-contain opacity-80 transition-opacity duration-300" />
              </div>
            </div>
          </a>
        {/each}
      </div>
    </div>
  </section>
</div>
