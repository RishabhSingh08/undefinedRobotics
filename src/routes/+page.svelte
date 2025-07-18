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

  const cards = [
    {
      title: "Culture of Learning & STEM",
      description: "Promoting a vibrant culture of learning and STEM engagement within our community, making education fun and accessible."
    },
    {
      title: "Hands-on Practical Skills",
      description: "Offering immersive, hands-on experiences where young people develop practical skills in engineering, programming, and problem-solving."
    },
    {
      title: "Teamwork & Community Outreach",
      description: "Fostering collaboration, creativity, and outreach by actively giving back to our community and inspiring the next generation."
    },
    {
      title: "Robotics for Everyone",
      description: "Believing that robotics is for all, empowering every student to achieve success and acquire essential skills, regardless of background."
    }
  ];

  // Array of sponsor images for easy iteration
  const sponsors = [s, s1, s2, s3, s4, s5, s6];
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

  /* Keyframes for the scrolling carousel */
  @keyframes scroll-left {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%); /* Scroll to the middle of the duplicated content */
    }
  }

  .carousel-container {
    overflow: hidden;
    white-space: nowrap; /* Prevent items from wrapping */
  }

  .carousel-track {
    display: inline-flex; /* Keep items in a single line */
    animation: scroll-left 20s linear infinite; /* Adjust duration for speed */
  }

  .carousel-track:hover {
    animation-play-state: paused; /* Pause on hover */
  }

  .carousel-item {
    display: inline-block; /* Ensure images stay in line */
    padding: 0 5rem; /* Spacing between logos */
    flex-shrink: 0; /* Prevent items from shrinking */
  }
</style>

<main class="text-white min-h-screen overflow-hidden  relative dm-sans">
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

  <section class="relative z-10">
    <div class="py-44 min-h-screen flex items-center justify-center overflow-hidden">
      <div class="absolute inset-0 z-0">
        <div class="absolute inset-0 bg-gradient-to-r from-yellow-500 to-yellow-200 rounded-full blur-3xl opacity-5 transform -translate-y-1/2 "></div>
        <div class="absolute inset-0 bg-gradient-to-r from-yellow-200 to-yellow-700 rounded-full blur-3xl opacity-5 transform translate-y-1/2"></div>
      </div>

      <div class="z-20 max-w-7xl mx-auto px-4 flex flex-col items-center">
        <div class="space-y-16 text-center">
          <div class="lg:col-span-3 flex justify-center">
            <div class="relative  ">
              <div class="absolute inset-0 bg-gradient-to-r from-yellow-500 to-yellow-200 rounded-full blur-3xl opacity-20 z-0"></div>
              <img src={IconLogo} alt="Undefined Robotics Logo" class="md:w-80 w-36 relative z-10"/>
            </div>
          </div>

          <div class="space-y-12">
            <h1 class="text-4xl md:text-8xl tracking-wider lg:h-24">
              UNDEFINED ROBOTICS
            </h1>
            <p class="text-xl md:text-2xl text-gray-400 max-w-2xl mx-auto ">
              A high school level private robotics team based in Plano, Texas, promoting a culture of learning and STEM in our community.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center"> 
              <a href="/impact">
                <button class="bg-white text-black px-8 py-4 rounded-full text-lg hover:bg-gray-200 transition-colors group">
                    Our Impact
                    <span class="inline-block transition-transform group-hover:translate-x-1 ml-2">→</span>
                </button>
              </a>
              <a href="/record">
                  <button class="border border-white px-8 py-4 rounded-full text-lg hover:bg-white hover:text-black transition-colors">
                      View Our Achievements
                  </button>
              </a>
          </div>

          </div>
          <div class=" flex flex-col items-center animate-bounce ">
            <span class="text-md text-gray-400 mb-2">Learn more about us</span>
            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
            </svg>
        </div>

        </div>
      </div>

      <div class="absolute top-1/4 left-10 w-24 h-24 bg-yellow-200 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob z-0"></div>
      <div class="absolute top-1/3 right-10 w-24 h-24 bg-yellow-500 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-2000 z-0"></div>
      <div class="absolute bottom-1/4 left-1/3 w-24 h-24 bg-yellow-700 rounded-full mix-blend-multiply filter blur-xl opacity-10 animate-blob animation-delay-4000 z-0"></div>
    </div>

  
    
  </section>
  <section class="relative z-10 overflow-hidden">
    <div class="w-full flex justify-center items-center min-h-[500px]">
      <div class="relative w-full h-full">
        <img src={TeamPhoto} alt="Undefined Robotics Team" class="w-full h-full object-cover rounded-none" />
        <div class="absolute bottom-8 right-8">
          <a href="/team">
            <button class="border border-white px-8 py-4 rounded-full text-lg hover:bg-white hover:text-black transition-colors duration-300 backdrop-blur-sm bg-white/20">
              View Our Team
            </button>
          </a>
        </div>
      </div>
    </div>
  </section>


  <section id="mission" class="px-4 py-32 relative z-10">
    <div class="max-w-6xl mx-auto text-center">

      <p class="text-4xl md:text-6xl font-semibold text-center text-gray-100 tracking-tight mb-8">
        Our Mission
      </p>
      
      <div class="space-y-12 max-w-5xl mx-auto  ">

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          Undefined Robotics is a high school level private robotics team based in Plano, Texas. Our goal as a team is to promote a culture of learning and STEM in our community.
        </p>

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          We believe robotics is a great way to make STEM education and participation fun and engaging, especially for young people who are able to practice and learn practical skills through a hands-on and collaborative approach.
        </p>

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          We strongly believe that robotics is for everyone and that anyone can be successful, not only as members of our robotics team, but also in learning and acquiring important skills through robotics.
        </p>

        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed">
          As a community-based team, we hope to give back as much as possible by instilling this knowledge in students and young people in our own community.
        </p>

        <p class="text-xl md:text-2xl cedarville-cursive-regular text-right">
          ~ The Undefined Robotics team
        </p>
      </div>
    </div>
  </section>





  <section id="events" class="px-4 py-32 relative z-10">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-20">
        <p class="text-4xl md:text-6xl font-semibold text-center text-gray-100 tracking-tight mb-8">
          Events & Projects
        </p>
        </div>

      <div class="grid lg:grid-cols-3 gap-12 mb-16">
        <!-- Current Project -->
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <div class="flex items-center mb-6">
            <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3 animate-pulse"></div>
            <h3 class="text-2xl font-bold text-yellow-300">Current Project</h3>
          </div>
          <h4 class="text-xl font-semibold text-white mb-4">FTC Competition Robot 2025</h4>
          <p class="text-gray-300 leading-relaxed mb-4">
            Designing and building an autonomous robot for the FIRST Tech Challenge "INTO THE DEEP" season. Our focus is on creating innovative solutions for underwater-themed challenges.
          </p>
          <div class="flex items-center text-sm text-gray-400">
            <span class="mr-4">Status: In Progress</span>
            <span>Due: February 2025</span>
          </div>
        </div>

        <!-- Most Recent Event -->
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <div class="flex items-center mb-6">
            <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
            <h3 class="text-2xl font-bold text-green-300">Most Recent Event</h3>
          </div>
          <h4 class="text-xl font-semibold text-white mb-4">Dallas Regional Qualifier</h4>
          <p class="text-gray-300 leading-relaxed mb-4">
            Competed against 32 teams from across North Texas. Our robot performed exceptionally in autonomous mode, securing 3rd place overall and advancing to state championships.
          </p>
          <div class="flex items-center text-sm text-gray-400">
            <span class="mr-4">Date: January 15, 2025</span>
            <span>Result: 3rd Place</span>
          </div>
        </div>

        <!-- Season Highlights -->
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-8 border border-white/20 hover:bg-white/15 transition-all duration-300">
          <h3 class="text-2xl font-bold text-blue-300 mb-6">Season Highlights</h3>
          <div class="space-y-4">
            <div class="flex items-start">
              <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
              <div>
                <p class="text-white font-semibold">Innovation Award</p>
                <p class="text-gray-400 text-sm">Recognized for creative engineering solutions</p>
              </div>
            </div>
            <div class="flex items-start">
              <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
              <div>
                <p class="text-white font-semibold">Community Impact</p>
                <p class="text-gray-400 text-sm">Mentored 150+ students this season</p>
              </div>
            </div>
            <div class="flex items-start">
              <div class="w-2 h-2 bg-yellow-400 rounded-full mt-2 mr-3 flex-shrink-0"></div>
              <div>
                <p class="text-white font-semibold">Team Growth</p>
                <p class="text-gray-400 text-sm">Expanded from 8 to 15 active members</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Upcoming Events -->
      <div class="bg-white/5 backdrop-blur-sm rounded-xl p-8 border border-white/10">
        <h3 class="text-3xl font-bold text-white mb-8 text-center">Upcoming Events</h3>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              JUL 25
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Summer Workshop Series</h4>
              <p class="text-gray-400 text-sm">Introduction to robotics for beginners</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              AUG 12
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Community Outreach Day</h4>
              <p class="text-gray-400 text-sm">STEM demonstrations at local libraries</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              AUG 30
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Season Kickoff</h4>
              <p class="text-gray-400 text-sm">New challenge reveal and team planning</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              SEP 15
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Fundraising Gala</h4>
              <p class="text-gray-400 text-sm">Annual fundraising event for equipment</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              OCT 10
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">Scrimmage Tournament</h4>
              <p class="text-gray-400 text-sm">Practice matches with regional teams</p>
            </div>
          </div>
          
          <div class="flex items-start space-x-4">
            <div class="bg-yellow-400 text-black px-3 py-1 rounded-full text-sm font-bold flex-shrink-0">
              NOV 22
            </div>
            <div>
              <h4 class="text-lg font-semibold text-white">League Tournament</h4>
              <p class="text-gray-400 text-sm">First official competition of the season</p>
            </div>
          </div>
        </div>
      </div>

  </section>
  <section class="w-full py-8 overflow-hidden relative z-10">
    <div class="carousel-container bg-white/10 py-6">
      <div class="carousel-track">
        {#each [...sponsors, ...sponsors] as sponsor, i} <div class="carousel-item">
            <img src={sponsor} alt="Sponsor Logo {i + 1}" class="h-16 sm:h-20 max-w-none" />
          </div>
        {/each}
      </div>
    </div>
  </section>


</main>

