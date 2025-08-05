<script>
  import IconLogo from "../lib/images/logo.png";
  import TeamPhoto from "../lib/images/team.png";

  import s from "../lib/images/sponsors/s.png";
  import s1 from "../lib/images/sponsors/s1.png";
  import s2 from "../lib/images/sponsors/s2.png";
  import s3 from "../lib/images/sponsors/s3.png";
  import s4 from "../lib/images/sponsors/s4.png";
  import s5 from "../lib/images/sponsors/s5.png";
  import s6 from "../lib/images/sponsors/s6.png";
  import s7 from "../lib/images/sponsors/s7.png";

  const sponsors = [
    { src: s, href: 'https://www.cafelltech.com/' },
    { src: s1, href: 'https://hackclub.com/' },
    { src: s2, href: 'https://polymaker.com/' },
    { src: s3, href: 'https://www.twc.texas.gov/' },
    { src: s4, href: 'https://dekaresearch.com/' },
    { src: s5, href: 'https://www.bosch.com/' },
    { src: s6, href: 'https://www.jabil.com/' },
    { src: s7, href: 'https://www.solaceglobal.world/' }
  ];

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

  .carousel-container {
    overflow: hidden;
    white-space: nowrap; 
  }

  .carousel-track {
    display: inline-flex; 
    animation: scroll-left 20s linear infinite; 
  }

  .carousel-track:hover {
    animation-play-state: paused; 
  }

  .carousel-item {
    display: inline-block; 
    padding: 0 5rem; 
    flex-shrink: 0; 
  }
</style>

<main class="text-white overflow-hidden  relative dm-sans">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

    <section class="relative z-10">
<div class="h-screen flex items-center justify-center overflow-hidden relative">


  <div class="z-20 max-w-7xl mx-auto px-4 flex flex-col items-center h-full justify-center">
    <div class="space-y-6 sm:space-y-8 md:space-y-12 text-center">
      <div class="lg:col-span-3 flex justify-center">
        <div class="relative">
          <div class="absolute inset-0 bg-gradient-to-r from-yellow-500 to-yellow-200 rounded-full blur-3xl opacity-20 z-0"></div>
          <img src={IconLogo} alt="Undefined Robotics Logo" class="w-48 sm:w-48 md:w-64 lg:w-80 xl:w-96 relative z-10"/>
        </div>
      </div>

      <div class="space-y-4 sm:space-y-6 md:space-y-8">
        <h1 class="text-3xl sm:text-5xl md:text-6xl lg:text-5xl xl:text-7xl tracking-wider">
          UNDEFINED ROBOTICS
        </h1>
        <p class="text-sm sm:text-base md:text-lg lg:text-xl xl:text-2xl text-gray-400 max-w-2xl mx-auto px-4">
          One of the largest student-led STEM and robotics 501(c)3 non-profit organizations in Texas. Based in Dallas-Fort Worth but serve around the world.
        </p>
        <div class="flex flex-col sm:flex-row gap-3 md:gap-4 justify-center px-4"> 
          <a href="/impact">
            <button class="bg-white text-black px-4 sm:px-6 md:px-8 py-2 sm:py-3 md:py-4 rounded-full text-sm sm:text-base md:text-lg hover:bg-gray-200 transition-colors group hover:cursor-pointer">
              Our Impact
              <span class="inline-block transition-transform group-hover:translate-x-1 ml-2">→</span>
            </button>
          </a>
          <a href="/record">
            <button class="border border-white px-4 sm:px-6 md:px-8 py-2 sm:py-3 md:py-4 rounded-full text-sm sm:text-base md:text-lg hover:bg-white hover:text-black transition-colors hover:cursor-pointer">
              View Our Achievements
            </button>
          </a>
        </div>
      </div>
    </div>
    
    <div class="absolute bottom-[1%] left-1/2 transform -translate-x-1/2 z-20 flex flex-col items-center animate-bounce opacity-70">
      <span class="text-xs sm:text-normal md:text-lg">Learn more about us</span>
      <svg class="w-6 h-6 sm:w-7 sm:h-7 md:w-6 md:h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
      </svg>
    </div>
  </div>
  
</div>
    </section>


    <section class="relative z-10 overflow-hidden">
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
    </section>


  <section id="mission" class="px-4 py-32 relative z-10">
    <div class="max-w-6xl mx-auto text-center">

      <p class="text-4xl md:text-6xl font-semibold text-center text-gray-100 tracking-tight mb-8">
        Our Mission: Serve the Underserved
      </p>
      
      <div class="space-y-12 max-w-5xl mx-auto  ">

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          STEM should be for everyone.

        </p>

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          Yet, far too often, underrepresented groups—women, senior citizens, tribal and native communities, and non-English speakers—are left out of these opportunities. After witnessing the toxic and exclusionary culture that can surround robotics and STEM at our school robotics club competitions, we made it our mission to change that.
        </p>

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          We believe various backgrounds bring fresh perspective and innovation to STEM. Instead of just meeting a diversity quota or lowering the standard for certain groups, we staunchly believe in actually addressing the problem by building opportunities and resources for those underserved to learn, build, and thrive in STEM.
        </p>

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          Through education, outreach, hands-on opportunities, and real-world interactions, we strive to foster an open environment where everyone, regardless of background, can flourish.
        </p>

        <p class="text-xl md:text-2xl cedarville-cursive-regular text-right">
          ~ The Undefined Robotics team
        </p>
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
                <h3 class="text-2xl font-bold text-yellow-300">Our Robot</h3>
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
            <h3 class="text-2xl font-bold text-green-300">Most Recent Event</h3>
          </div>
          <h4 class="text-xl font-semibold text-white mb-4">Manufacturing Facility Tour</h4>
          <p class="text-gray-300 leading-relaxed mb-4">
            Our team had the opportunity to tour a local manufacturing facility, where we engaged in meaningful discussions with industry professionals and explored real-world applications of automation and engineering. It was an inspiring experience that opened the door for potential future collaboration.


          </p>
          <div class="flex items-center text-sm text-gray-400">
            <span class="mr-4">Date: July 25, 2025</span>
          </div>
        </div>

        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <h3 class="text-2xl font-bold text-blue-300 mb-6">Recent Developments</h3>
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
                <p class="text-gray-400 text-sm">Missing Amps #30801 joins Undefined Robotics NPO</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="bg-white/5 backdrop-blur-sm rounded-xl p-8 border border-white/10">
        <h3 class="text-3xl font-bold text-white mb-8 text-center">Upcoming Events</h3>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              AUG 5
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Website Revamp Launch</h4>
              <p class="text-gray-400 text-sm">Version 2 launch of new NPO website</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              AUG 12
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">High School Begins</h4>
              <p class="text-gray-400 text-sm">Summer projects and iniatives wrap up</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              SEP 6
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Est. Season Kickoff</h4>
              <p class="text-gray-400 text-sm">New FTC challenge reveal and team planning</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              NOV #
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">1st League meet</h4>
              <p class="text-gray-400 text-sm">First robot competition of the season</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              DEC 13
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">NLSS STEM Event</h4>
              <p class="text-gray-400 text-sm">Major outreach event educating in STEM thru kits</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
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
<section class="w-full overflow-hidden relative z-10 bg-white/10 mb-32">

  
  <div class="carousel-container py-6">
    <div class="carousel-track">
      {#each [...sponsors, ...sponsors] as sponsor, i}
        <div class="carousel-item">
          <a href={sponsor.href} target="_blank" rel="noopener noreferrer" aria-label="Sponsor {i + 1}">
            <img src={sponsor.src} alt="Sponsor Logo {i + 1}" class="h-16 sm:h-20 max-w-none" />
          </a>
        </div>
      {/each}
    </div>
  </div>
</section>

</main>

