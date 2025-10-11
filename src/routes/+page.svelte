<script>
  import { onMount, onDestroy } from 'svelte';
  import IconLogo from "../lib/images/logo.png";
  import TeamPhoto from "../lib/images/team.png";

  import hero1 from "../lib/images/hero/1.JPG";
  import hero2 from "../lib/images/hero/2.JPG";
  import hero3 from "../lib/images/hero/3.JPG";
  import hero4 from "../lib/images/hero/4.JPG";
  import hero5 from "../lib/images/hero/5.png";
  import hero6 from "../lib/images/hero/6.png";
  import hero7 from "../lib/images/hero/7.png";
  import hero8 from "../lib/images/hero/8.png";
  import hero9 from "../lib/images/hero/9.png";
  import hero10 from "../lib/images/hero/10.png";
  import hero11 from "../lib/images/hero/11.png";
  import hero12 from "../lib/images/hero/12.png";


  import s from "../lib/images/sponsors/s.png";
  import s1 from "../lib/images/sponsors/s1.png";
  import s2 from "../lib/images/sponsors/s2.png";
  import s3 from "../lib/images/sponsors/s3.png";
  import s4 from "../lib/images/sponsors/s4.png";
  import s5 from "../lib/images/sponsors/s5.png";
  import s6 from "../lib/images/sponsors/s6.png";
  import s7 from "../lib/images/sponsors/s7.png";
  
  import AdBanner from "../lib/images/sponsors/AdBanner.png";
  import Ad1 from "../lib/images/sponsors/Ad1.png";
  import Ad2 from "../lib/images/sponsors/Ad2.png";

  const sponsors = [
    { src: s, href: 'https://www.cafelltech.com/' },
    { src: s1, href: 'https://hackclub.com/' },
    { src: s2, href: 'https://polymaker.com/' },
    { src: s3, href: 'https://www.twc.texas.gov/' },
    { src: s4, href: 'https://dekaresearch.com/' },
    { src: s5, href: 'https://www.bosch.com/' },
    { src: s6, href: 'https://www.jabil.com/' },
    // { src: s7, href: 'https://www.solaceglobal.world/' }
  ];

  const heroImages = [hero1, hero2, hero3, hero4, hero5, hero6, hero7, hero8, hero9, hero10, hero11, hero12];
  
  // Create 3 columns with different image arrangements
  const column1 = [hero8, hero6, hero12, hero9];
  const column2 = [hero5, hero10, hero7, hero11];
  const column3 = [hero2, hero4, hero1, hero3];

  let currentHeroIndex = 0;

  onMount(() => {
    const heroInterval = setInterval(() => {
      currentHeroIndex = (currentHeroIndex + 1) % heroImages.length;
    }, 4000);

    return () => {
      clearInterval(heroInterval);
    };
  });

</script>

<style>
  .dm-sans {
    font-family: "DM Sans", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
  }
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

  @keyframes scroll-left {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%); 
    }
  }

  .sponsor-carousel-container {
    overflow: hidden;
    white-space: nowrap; 
  }

  .sponsor-carousel-track {
    display: inline-flex; 
    animation: scroll-left 20s linear infinite; 
  }

  .sponsor-carousel-item {
    display: inline-block; 
    padding: 0 5rem; 
    flex-shrink: 0; 
  }

  @keyframes scroll-vertical {
    0% {
      transform: translateY(0);
    }
    100% {
      transform: translateY(-100%);
    }
  }

  .carousel-column {
    overflow: hidden;
    position: relative;
    height: 100vh;
  }

  .carousel-track {
    display: flex;
    flex-direction: column;
    animation: scroll-vertical linear infinite;
  }

  .carousel-track-1 {
    animation-duration: 90s;
  }

  .carousel-track-2 {
    animation-duration: 110s;
  }

  .carousel-track-3 {
    animation-duration: 100s;
  }

  .carousel-image {
    width: 100%;
    height: 33.333vh;
    object-fit: cover;
    flex-shrink: 0;
  }

  .hero-bg-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0;
    transition: opacity 1s ease-in-out;
  }

  .hero-bg-image.active {
    opacity: 1;
  }

  .hero-background-grid {
    position: absolute;
    inset: 0;
    background: radial-gradient(rgba(255,255,255,0.2) 1px, transparent 1px);
    background-size: 80px 80px;
    mask-image: linear-gradient(to bottom, transparent 0%, rgba(0,0,0,0.3) 40%, rgba(0,0,0,0.8) 100%);
    -webkit-mask-image: linear-gradient(to bottom, transparent 0%, rgba(0,0,0,0.3) 40%, rgba(0,0,0,0.8) 100%);
    pointer-events: none;
    z-index: 1;
  }
</style>

<main class="text-white overflow-hidden  relative dm-sans">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <!-- hero section -->
    <section class="relative z-10 overflow-hidden ">
      
      <!-- Desktop: 3 Column Vertical Carousel -->
      <div class="hidden lg:flex w-full h-screen relative">
        
        <!-- Column 1 - Slow Speed (20s) -->
        <div class="carousel-column flex-1">
          <div class="carousel-track carousel-track-1">
            {#each [...column1, ...column1, ...column1] as image}
              <img src={image} alt="Team" class="carousel-image" />
            {/each}
          </div>
        </div>

        <!-- Column 2 - Medium Speed (25s) -->
        <div class="carousel-column flex-1">
          <div class="carousel-track carousel-track-2">
            {#each [...column2, ...column2, ...column2] as image}
              <img src={image} alt="Team" class="carousel-image" />
            {/each}
          </div>
        </div>

        <!-- Column 3 - Fast Speed (30s) -->
        <div class="carousel-column flex-1">
          <div class="carousel-track carousel-track-3">
            {#each [...column3, ...column3, ...column3] as image}
              <img src={image} alt="Team" class="carousel-image" />
            {/each}
          </div>
        </div>
      </div>

      <!-- Mobile: Slideshow Background -->
      <div class="lg:hidden relative h-auto min-h-[600px]">
        {#each heroImages as image, idx}
          <div class="hero-bg-image" class:active={idx === currentHeroIndex}>
            <img src={image} alt="Team {idx + 1}" class="w-full h-full object-cover" />
          </div>
        {/each}
      </div>

      <!-- Gradient Overlay -->
      <div class="absolute inset-0 bg-gradient-to-t from-black via-black/70 to-black/30 pointer-events-none z-20"></div>

      <!-- Ad Banner - Top Center (Desktop only) -->
      <div class="hidden lg:block absolute top-4 lg:top-24 left-1/2 transform -translate-x-1/2 z-30">
        <img 
          src={AdBanner} 
          alt="Sponsor Banner" 
          class="h-12 md:h-16 lg:h-24 w-auto rounded-lg"
        />
      </div>

      <!-- Text Overlay - Centered on Mobile, Bottom Left on Desktop -->
      <div class="absolute inset-0 lg:inset-auto lg:bottom-0 lg:left-0 z-30 flex items-center justify-center lg:block p-6 md:p-14 lg:p-20 max-w-4xl">
        <div class="text-center lg:text-left w-full">
          <!-- Logo and Title -->
          <div class="flex flex-col items-center lg:flex-row lg:items-center gap-4 sm:gap-6 mb-6">
            <img 
              src={IconLogo} 
              alt="Undefined Robotics Logo" 
              class="w-20 sm:w-24 md:w-32 lg:w-40"
            />
            <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold tracking-tight">
              UNDEFINED<br/>
              <span class="text-yellow-400">ROBOTICS</span>
            </h1>
          </div>

          <!-- Description -->
          <p class="text-base sm:text-lg md:text-xl lg:text-2xl text-gray-200 leading-relaxed mb-8">
            One of the largest student-led STEM and robotics 501(c)3 non-profit projects in Texas. Based in Dallas-Fort Worth but serve around the world.
          </p>

          <!-- Buttons -->
          <div class="flex flex-col sm:flex-row gap-3 pointer-events-auto justify-center lg:justify-start">
            <a href="/impact" class="w-full sm:w-auto">
              <button class="w-full bg-gradient-to-r from-yellow-400 to-yellow-500 text-black px-6 py-3 rounded-lg text-base font-semibold hover:from-yellow-500 hover:to-yellow-600 transition-all duration-200 group shadow-lg">
                Our Impact
                <span class="inline-block transition-transform group-hover:translate-x-1 ml-2">→</span>
              </button>
            </a>
            <a href="/record" class="w-full sm:w-auto">
              <button class="w-full bg-gradient-to-r from-transparent to-transparent border-2 border-yellow-400 text-yellow-400 px-6 py-3 rounded-lg text-base font-semibold hover:from-yellow-400 hover:to-yellow-500 hover:text-black hover:border-transparent transition-all duration-200 shadow-lg">
                View Our Achievements
              </button>
            </a>
          </div>
        </div>
      </div>
    </section>


    <!-- <section class="relative z-10 overflow-hidden">
      <div class="w-full flex justify-center items-center min-h-[500px]">
        <div class="relative w-full h-full">
          <img src={TeamPhoto} alt="Undefined Robotics Team" class="w-full h-full object-cover rounded-none" />
          <div class="absolute bottom-8 right-8">
            <a href="/family">
              <button class="border border-white px-8 py-4 rounded-full text-lg hover:bg-white hover:text-black transition-colors duration-300 backdrop-blur-sm bg-white/20 hover:cursor-pointer">
                View Our Family
              </button>
            </a>
          </div>
        </div>
      </div>
    </section> -->


  <section id="mission" class="px-4 py-32 relative z-10">
    <div class="max-w-6xl mx-auto text-center">

      <p class="text-4xl md:text-6xl font-semibold text-center text-gray-100 tracking-tight mb-8">
        Our Mission: Serve the Underserved
      </p>
      
      <div class="space-y-10 max-w-5xl mx-auto  ">

        <p class="text-xl md:text-3xl text-gray-300 leading-relaxed">
          STEM should be for everyone.

        </p>

        <p class="text-xl md:text-3xl text-gray-300 leading-relaxed">
          Yet, far too often, underrepresented groups—women, senior citizens, tribal and native communities, and non-English speakers—are left out of these opportunities. After witnessing the toxic and exclusionary culture that can surround robotics and STEM at our school robotics club competitions, we made it our mission to change that.
        </p>

        <p class="text-xl md:text-3xl text-gray-300 leading-relaxed">
          We believe various backgrounds bring fresh perspective and innovation to STEM. Instead of just meeting a diversity quota or lowering the standard for certain groups, we staunchly believe in actually addressing the problem by building opportunities and resources for those underserved to learn, build, and thrive in STEM.
        </p>

        <p class="text-xl md:text-3xl text-gray-300 leading-relaxed">
          Through education, outreach, hands-on opportunities, and real-world interactions, we strive to foster an open environment where everyone, regardless of background, can flourish.
        </p>

        <p class="text-xl md:text-2xl cedarville-cursive-regular text-center md:text-right">
          ~ The Undefined Robotics team
        </p>
      </div>
    </div>
  </section>
  <div class="max-w-7xl mx-auto px-4">
  <div class="grid grid-cols-2 md:grid-cols-5 gap-6 md:gap-8 mb-20">
    <div class="text-center">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">$25K+</div>
      <div class="text-gray-300">Value Raised</div>
    </div>
    <div class="text-center">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">4,000+</div>
      <div class="text-gray-300">Underserved Individuals Reached</div>
    </div>
    <div class="text-center">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">36+</div>
      <div class="text-gray-300">FTC Teams Connected</div>
    </div>
    <div class="text-center">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">10+</div>
      <div class="text-gray-300">Regional/National Awards</div>
    </div>
    <div class="text-center">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">15+</div>
      <div class="text-gray-300">Proffesionals Connected</div>
    </div>
  </div>
  </div>
  
<hr
  class="my-12 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />

  <!-- Sponsor Ads Section -->
  <section class="px-4 relative z-10">
    <div class="max-w-7xl mx-auto">
      <!-- Ad Banner - Mobile Only (Above Sponsor Ads) -->
      <div class="md:hidden flex justify-center mb-8">
        <img 
          src={AdBanner} 
          alt="Sponsor Banner" 
          class="h-16 w-auto rounded-lg"
        />
      </div>
      
      <div class="grid md:grid-cols-2 gap-8">
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
          <img 
            src={Ad1} 
            alt="Sponsor Advertisement 1" 
            class="w-full h-auto rounded-lg"
          />
        </div>
        <div class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
          <img 
            src={Ad2} 
            alt="Sponsor Advertisement 2" 
            class="w-full h-auto rounded-lg"
          />
        </div>
      </div>
    </div>
  </section>

<hr
  class="my-12 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />
  <section id="events" class="px-4 pt-16 pb-32 relative z-10">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-20">
        <p class="text-4xl md:text-6xl font-semibold text-center text-gray-100 tracking-tight mb-8">
          Events & Projects
        </p>
        </div>

      <div class="grid lg:grid-cols-3 gap-12 mb-16">
        <a href="/robot" class="block group h-full">
          <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 group-hover:bg-white/15 transition-all duration-300 h-full flex flex-col">
            <div>
              <div class="flex items-center mb-6">
                <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3 animate-pulse"></div>
                <h3 class="text-2xl font-bold bg-gradient-to-r from-yellow-200 to-yellow-400 bg-clip-text text-transparent">Our Robot</h3>
              </div>
              <h4 class="text-xl font-semibold text-white mb-4">FTC Competition Robot 2025</h4>
              <p class="text-gray-300 leading-relaxed mb-4">
                Designing and building an autonomous robot for the FIRST Tech Challenge "INTO THE DEEP" season. Our focus is on creating innovative solutions for underwater-themed challenges.
              </p>
            </div>
            <div class="flex items-center text-sm text-gray-400 mt-auto">
              <span class="mr-4">Status: Finished</span>
            </div>
          </div>
        </a>

        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <div class="flex items-center mb-6">
            <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
            <h3 class="text-2xl font-bold bg-gradient-to-r from-green-200 to-green-400 bg-clip-text text-transparent">Most Recent Event</h3>
          </div>
          <h4 class="text-xl font-semibold text-white mb-4">Manufacturing Facility Tour</h4>
          <p class="text-gray-300 leading-relaxed mb-4">
            Our team had the opportunity to tour a local manufacturing facility, where we engaged in meaningful discussions with industry professionals and explored real-world applications of automation and engineering.


          </p>
          <div class="flex items-center text-sm text-gray-400">
            <span class="mr-4">Date: August 1st, 2025</span>
          </div>
        </div>

        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <h3 class="text-2xl font-bold bg-gradient-to-r from-blue-200 to-blue-400 bg-clip-text text-transparent mb-6">Recent Developments</h3>
          <div class="space-y-4">
            <div class="flex items-start">
              <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
              <div>
                <p class="text-white font-semibold">New v2 website launch</p>
                <p class="text-gray-400 text-sm">Much anticipated website revamp drops August 5th</p>
              </div>
            </div>
            <div class="flex items-start">
              <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
              <div>
                <p class="text-white font-semibold">Socials updated</p>
                <p class="text-gray-400 text-sm">Exciting new updates to our socials as we gear up for season</p>
              </div>
            </div>
            <div class="flex items-start">
              <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
              <div>
                <p class="text-white font-semibold">Acquired new team</p>
                <p class="text-gray-400 text-sm">Missing Amps #30801 joins Undefined Robotics NPP</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="bg-white/5 backdrop-blur-sm rounded-xl p-8 border border-white/10">
        <h3 class="text-3xl font-bold text-white mb-8 text-center">Upcoming Events</h3>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="flex items-start space-x-4">
            <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              AUG 5
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Website Revamp Launch</h4>
              <p class="text-gray-400 text-sm">Version 2 launch of new NPP website</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              AUG 12
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">High School Begins</h4>
              <p class="text-gray-400 text-sm">Summer projects and iniatives wrap up</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              SEP 6
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Est. Season Kickoff</h4>
              <p class="text-gray-400 text-sm">New FTC challenge reveal and team planning</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              NOV #
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">1st League meet</h4>
              <p class="text-gray-400 text-sm">First robot competition of the season</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              DEC 13
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">NLSS STEM Event</h4>
              <p class="text-gray-400 text-sm">Major outreach event educating in STEM thru kits</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              JAN #
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">League Tournament</h4>
              <p class="text-gray-400 text-sm">First official tournament of the season</p>
            </div>
          </div>
        </div>
      </div>
      </div>

      
  </section>
  <hr
  class="mb-12 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />

  <h2 class="text-4xl sm:text-7xl  text-center text-white mt-32 mb-24 cedarville-cursive-regular">
  Thank You to Our Sponsors and Partners!
  </h2>


<section class="w-full overflow-hidden relative z-10  mb-32">
  <div class="block md:hidden px-4 py-8">
    <div class="grid grid-cols-2 gap-6 max-w-md mx-auto">
      {#each sponsors as sponsor, i}
        <a href={sponsor.href} target="_blank" rel="noopener noreferrer" aria-label="Sponsor {i + 1}" class="flex items-center justify-center p-4 bg-white/20 rounded-lg hover:bg-white/10 transition-all">
          <img src={sponsor.src} alt="Sponsor Logo {i + 1}" class="h-12 w-auto max-w-full object-contain" />
        </a>
      {/each}
    </div>
  </div>
  
  <div class="hidden md:block sponsor-carousel-container py-6 bg-white/20">
    <div class="sponsor-carousel-track">
      {#each [...sponsors, ...sponsors] as sponsor, i}
        <div class="sponsor-carousel-item">
          <a href={sponsor.href} target="_blank" rel="noopener noreferrer" aria-label="Sponsor {i + 1}">
            <img src={sponsor.src} alt="Sponsor Logo {i + 1}" class="h-16 sm:h-20 max-w-none" />
          </a>
        </div>
      {/each}
    </div>
  </div>
</section>

</main>
