<script>
  import { onMount, onDestroy } from 'svelte';
  import IconLogo from "../lib/images/logo.png";
  import TeamPhoto from "../lib/images/team.png";

  import StatsGrid from '../lib/components/StatsGrid.svelte';
  import Sponsors from '../lib/components/Sponsors.svelte';

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


  
  import AdBanner from "../lib/images/sponsors/AdBanner.png";
  import Ad1 from "../lib/images/sponsors/Ad1.png";
  import Ad2 from "../lib/images/sponsors/Ad2.png";

  const heroImages = [hero1, hero2, hero3, hero4, hero5, hero6, hero7, hero8, hero9, hero10, hero11, hero12];
  
  // Create 3 columns with different image arrangements
  const column1 = [hero8, hero6, hero12, hero9];
  const column2 = [hero5, hero10, hero7, hero11];
  const column3 = [hero2, hero4, hero1, hero3];

  let currentHeroIndex = 0;

  const ourRobot = {
    subtitle: 'FTC Competition Robot 2025',
    description: 'Designing and building an autonomous robot for the FIRST Tech Challenge "INTO THE DEEP" season. Our focus is on creating innovative solutions for underwater-themed challenges.'
  };

  const recentEvent = {
    subtitle: 'Manufacturing Facility Tour',
    description: 'Our team had the opportunity to tour a local manufacturing facility, where we engaged in meaningful discussions with industry professionals and explored real-world applications of automation and engineering.'
  };

  const recentDevelopments = [
    { title: 'New v2 website launch', description: 'Much anticipated website revamp drops August 5th' },
    { title: 'Socials updated', description: 'Exciting new updates to our socials as we gear up for season' },
    { title: 'Acquired new team', description: 'Missing Amps #30801 joins Undefined Robotics NPP' }
  ];

  const upcomingEvents = [
    { date: 'SEP 06', title: 'Season Kickoff', description: 'New FTC challenge reveal and team planning' },
    { date: 'OCT 11', title: 'Website Update Drop', description: 'Version 2.1 of new NPP website' },
    { date: 'OCT 17', title: 'Build Show Expo', description: 'Come join us in this 2 day event'},
    { date: 'NOV 08', title: '1st League meet', description: 'First robot competition of the season' },
    { date: 'DEC 13', title: 'NLSS STEM Event', description: 'Major outreach event educating in STEM thru kits' },
    { date: 'JAN #', title: 'League Tournament', description: 'First official tournament of the season' }
  ];

  onMount(() => {
    const heroInterval = setInterval(() => {
      currentHeroIndex = (currentHeroIndex + 1) % heroImages.length;
    }, 4000);

    return () => {
      clearInterval(heroInterval);
    };
  });

</script>
<!-- SEO HEAD TAGS -->
<svelte:head>
  <title>Undefined Robotics | Home</title>
  <meta name="description" content="Undefined Robotics is one of Texas’ largest student-led STEM and robotics 501(c)3 nonprofit programs. We serve underserved and underrepresented communities through outreach, engineering education, and FTC robotics." />

  <!-- Canonical -->
  <link rel="canonical" href="https://undefinedrobotics.org/" />

  <!-- OpenGraph -->
  <meta property="og:title" content="Undefined Robotics | Student-Led STEM Nonprofit" />
  <meta property="og:description" content="A student-led 501(c)3 robotics nonprofit providing STEM education and outreach to underserved communities worldwide." />
  <meta property="og:image" content="/og-image.png" />
  <meta property="og:url" content="https://undefinedrobotics.org/" />
  <meta property="og:type" content="website" />

  <!-- Twitter -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Undefined Robotics | FTC Robotics Team & STEM Nonprofit" />
  <meta name="twitter:description" content="Empowering underserved communities through robotics education, engineering, and STEM outreach." />
  <meta name="twitter:image" content="/og-image.png" />

  <!-- Accessibility / indexing -->
  <meta name="robots" content="index, follow" />

  <!-- Schema.org JSON-LD -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "Undefined Robotics",
    "url": "https://undefinedrobotics.org",
    "logo": "https://undefinedrobotics.org/logo.png",
    "description": "Student-led 501(c)3 STEM & robotics nonprofit serving underserved communities.",
    "sameAs": [
      "https://instagram.com/undefinedrobotics",
      "https://twitter.com/undefinedrobotics",
      "https://youtube.com/undefinedrobotics"
    ]
  }
  </script>
</svelte:head>

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

</style>

<main class="text-white overflow-hidden  relative dm-sans">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <!-- hero section -->
    <section class="relative z-10 overflow-hidden pt-[80px] md:pt-0">
      
      <!-- Desktop: 3 Column Vertical Carousel -->
      <div class="hidden lg:flex w-full h-screen relative">
        
        <div class="carousel-column flex-1">
          <div class="carousel-track carousel-track-1">
            {#each [...column1, ...column1, ...column1] as image}
              <img src={image} alt="Team" class="carousel-image" />
            {/each}
          </div>
        </div>

        <div class="carousel-column flex-1">
          <div class="carousel-track carousel-track-2">
            {#each [...column2, ...column2, ...column2] as image}
              <img src={image} alt="Team" class="carousel-image" />
            {/each}
          </div>
        </div>

        <div class="carousel-column flex-1">
          <div class="carousel-track carousel-track-3">
            {#each [...column3, ...column3, ...column3] as image}
              <img src={image} alt="Team" class="carousel-image" />
            {/each}
          </div>
        </div>
      </div>

      <div class="lg:hidden relative h-auto min-h-[600px]">
        {#each heroImages as image, idx}
          <div class="hero-bg-image" class:active={idx === currentHeroIndex}>
            <img src={image} alt="Team {idx + 1}" class="w-full h-full object-cover" />
          </div>
        {/each}
      </div>

      <!-- Gradient Overlay -->
      <div class="absolute inset-0 bg-gradient-to-t from-black via-black/70 to-black/30 z-20"></div>

      <!-- Ad Banner - (Desktop only) -->

      <!-- Text Overlay - Centered on Mobile, Bottom Left on Desktop -->
      <div class="absolute inset-0 lg:inset-auto lg:bottom-0 lg:left-0 z-30 flex items-center justify-center lg:block p-6 md:p-14 lg:p-20 max-w-4xl animate-fade-right">
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
              <span class="bg-gradient-to-r from-yellow-400 to-yellow-200 bg-clip-text text-transparent">ROBOTICS</span>
            </h1>
          </div>

          <!-- Description -->
          <p class="text-base sm:text-lg md:text-xl lg:text-2xl text-gray-200 leading-relaxed mb-8">
One of the largest student-led STEM and robotics fiscally sponsored 501(c)3 nonprofit projects in Texas. Based in Dallas-Fort Worth but serve around the world.
          </p>

          <!-- Buttons -->
<div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start"> 
  <a href="/impact" class="w-full sm:w-auto"> 
    <button class="w-full h-[54px] bg-gradient-to-r from-yellow-400 to-yellow-300 text-black px-8 rounded-md hover:cursor-pointer text-base font-bold hover:from-yellow-300 hover:to-yellow-200 hover:shadow-[0_0_20px_rgba(250,204,21,0.5)] transition-all duration-300 shadow-xl flex items-center justify-center">
      Our Impact
      <span class="ml-2">→</span>
    </button> 
  </a> 
  <a href="/record" class="w-full sm:w-auto"> 
    <button class="w-full h-[54px] bg-transparent text-yellow-400 border-2 border-yellow-400 px-8 rounded-md hover:cursor-pointer text-base font-bold hover:bg-gradient-to-r hover:from-yellow-400 hover:to-yellow-300 hover:text-black hover:border-yellow-300 transition-all duration-300 shadow-xl flex items-center justify-center">
      View Our Achievements
    </button> 
  </a> 
</div>
        </div>
      </div>
    </section>

  <section id="mission" class="px-4 py-32 relative z-10 animate-fade">
    <div class="max-w-6xl mx-auto text-center">

      <p class="text-4xl md:text-6xl font-semibold text-center text-gray-100 tracking-tight mb-8">
        Our Mission: Serve the Underserved
      </p>
      
      <div class="space-y-10 max-w-5xl mx-auto  ">

        <p class="text-xl md:text-3xl text-gray-300 leading-relaxed">
          STEM should be for everyone.

        </p>

        <p class="text-xl md:text-3xl text-gray-300 leading-relaxed">
          Yet, far too often, underrepresented groups—abuse victims, senior citizens, tribal and native communities, and non-English speakers—are left out of these opportunities. After witnessing the toxic and exclusionary culture that can surround robotics and STEM at our school robotics club competitions, we made it our mission to change that.
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
  <div class="max-w-7xl mx-auto px-4 mb-20 relative z-30 animate-fade-up">
     <StatsGrid />
  </div>
  

<hr class="my-12 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />
  <section id="events" class="px-4 pt-16 pb-32 relative z-10 animate-fade-down">
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
          <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
          <h3 class="text-2xl font-bold bg-gradient-to-r from-yellow-200 to-yellow-400 bg-clip-text text-transparent">Our Robot</h3>
        </div>
        <h4 class="text-xl font-semibold text-white mb-4">{ourRobot.subtitle}</h4>
        <p class="text-gray-300 leading-relaxed mb-4">{ourRobot.description}</p>
      </div>
    </div>
  </a>

  <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
    <div class="flex items-center mb-6">
      <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
      <h3 class="text-2xl font-bold bg-gradient-to-r from-green-200 to-green-400 bg-clip-text text-transparent">Most Recent Event</h3>
    </div>
    <h4 class="text-xl font-semibold text-white mb-4">{recentEvent.subtitle}</h4>
    <p class="text-gray-300 leading-relaxed mb-4">{recentEvent.description}</p>
  </div>

  <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
    <div class="flex items-center mb-6">
      <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
      <h3 class="text-2xl font-bold bg-gradient-to-r from-blue-200 to-blue-400 bg-clip-text text-transparent">Recent Developments</h3>
    </div>
    <div class="space-y-4">
      {#each recentDevelopments as dev}
        <div class="flex items-start">
          <div class="mr-3">-</div>
          <div>
            <p class="text-white font-semibold">{dev.title}</p>
            <p class="text-gray-400 text-sm">{dev.description}</p>
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>

      <div class="bg-white/5 backdrop-blur-sm rounded-xl p-8 border border-white/10">
        <h3 class="text-3xl font-bold text-white mb-8 text-center">Upcoming Events</h3>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          {#each upcomingEvents as event}
            <div class="flex items-start space-x-4">
              <div class="text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
                {event.date}
              </div>
              <div>
                <h4 class="text-lg font-semibold text-white">{event.title}</h4>
                <p class="text-gray-400 text-sm">{event.description}</p>
              </div>
            </div>
          {/each}
        </div>
      </div>
      </div>

      
  </section>
  <hr
  class="mb-12 h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />


  <Sponsors />



</main>