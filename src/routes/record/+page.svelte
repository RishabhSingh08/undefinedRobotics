<script>
    import { onMount } from 'svelte';
    import hero5 from "../../lib/images/hero/5.png";
    import hero6 from "../../lib/images/hero/6.png";
    import hero12 from "../../lib/images/hero/12.png";
    
    import irsLetter from "../../lib/images/files/IRS Letter (1).pdf";
    import certificateOfStatus from "../../lib/images/files/Certificate of Status.pdf";
    import fiscalSponsorshipLetter from "../../lib/images/files/fiscal_sponsorship_letter (1).pdf";

    const carouselImages1 = [hero5, hero6];
    const carouselImages2 = [hero12];

    let currentIndex1 = 0;
    let currentIndex2 = 0;

    onMount(() => {
        const interval1 = setInterval(() => {
            currentIndex1 = (currentIndex1 + 1) % carouselImages1.length;
        }, 3000);

        const interval2 = setInterval(() => {
            currentIndex2 = (currentIndex2 + 1) % carouselImages2.length;
        }, 3500);

        return () => {
            clearInterval(interval1);
            clearInterval(interval2);
        };
    });

    const seasons = [
        {
            year: '2024-25 Season',
            nodeColor: 'bg-yellow-400',
            badgeBgColor: 'bg-yellow-400',
            badgeTextColor: 'text-gray-900',
            awards: [
                {
                    title: 'Control Award',
                    color: 'bg-violet-400',
                    locations: ['FiT-North Pre-Worlds Championship']
                },
                {
                    title: 'RTX Innovate Award',
                    color: 'bg-cyan-400',
                    locations: ['FiT-North Pre-Worlds Championship']
                },
                {
                    title: 'Connect Award',
                    color: 'bg-rose-400',
                    locations: ['Texas FTC Championship']
                },
                {
                    title: 'Finalist Alliance Captain',
                    color: 'bg-lime-400',
                    locations: ['Texas FTC Championship']
                },
                {
                    title: 'Winning Alliance',
                    color: 'bg-orange-400',
                    locations: ['FiT-North Pre-Worlds Championship']
                },
                {
                    title: 'Peak Top 100 Robot in the World',
                    color: 'bg-indigo-400',
                    locations: ['Semi-Area Competition']
                },
            ]
        },
        {
            year: '2023-24 Season',
            nodeColor: 'bg-blue-400',
            badgeBgColor: 'bg-blue-400',
            badgeTextColor: 'text-gray-900',
            awards: [
                {
                    title: 'Control Award - 2×',
                    color: 'bg-violet-400',
                    locations: ['FiT-North E&F Tournament', 'FiT-North Area Championship']
                },
                {
                    title: 'Design Award - 2×',
                    color: 'bg-indigo-400',
                    locations: ['FiT-North Last Call Qualifier']
                },
                {
                    title: 'RTX Innovate Award',
                    color: 'bg-cyan-400',
                    locations: ['FiT-North Last Call Qualifier']
                },
                {
                    title: 'Inspire Award',
                    color: 'bg-purple-400',
                    locations: ['FiT-North E&F Tournament']
                },
                {
                    title: 'Connect Award',
                    color: 'bg-rose-400',
                    locations: ['FiT-North Semi-Area Championship']
                },
                {
                    title: 'Winning Alliance',
                    color: 'bg-orange-400',
                    locations: ['Texas FTC UIL 6A State Championship']
                }
            ]
        }

    ];
</script>

<svelte:head>
  <title>Undefined Robotics | Record</title>
  <meta name="description" content="Explore the history of Undefined Robotics (Team #25782). View our FTC awards, including Inspire, Innovate, and Winning Alliance, plus our 501(c)(3) nonprofit documentation." />
  <meta name="keywords" content="FTC Awards, Inspire Award, Winning Alliance, Robotics Competition Record, 501(c)(3) Nonprofit, Undefined Robotics History, Hack Foundation" />

  <link rel="canonical" href="https://undefinedrobotics.org/record" />

  <meta property="og:title" content="Our Record | Undefined Robotics Awards & History" />
  <meta property="og:description" content="From Winning Alliance to the Inspire Award. See our journey through the FIRST Tech Challenge seasons and our nonprofit milestones." />
  <meta property="og:image" content="https://undefinedrobotics.org/record-og.png" />
  <meta property="og:url" content="https://undefinedrobotics.org/record" />
  <meta property="og:type" content="website" />

  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Undefined Robotics Competition Record" />
  <meta name="twitter:description" content="Our trophy case and legal standing. See how we are making an impact in STEM." />
  <meta name="twitter:image" content="https://undefinedrobotics.org/record-og.png" />

  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "NGO",
    "name": "Undefined Robotics",
    "funder": {
        "@type": "Organization",
        "name": "The Hack Foundation"
    },
    "awards": [
        "Inspire Award",
        "Winning Alliance",
        "RTX Innovate Award",
        "Control Award",
        "Connect Award",
        "Design Award"
    ],
    "description": "A student-led 501(c)(3) robotics nonprofit with a history of excellence in FIRST Tech Challenge."
  }
  </script>
</svelte:head>

<style>
  .slideshow-carousel {
    width: 700px;
    height: 400px;
    position: relative;
    overflow: hidden;
    border-radius: 12px;
  }

  .slideshow-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    transition: opacity 0.5s ease-in-out;
  }

  .slideshow-image.active {
    opacity: 1;
  }
</style>

<section id="record" class="px-6 md:px-8 lg:px-10 py-32 relative z-10 min-h-screen">
    <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

    <div class="max-w-[105rem] mx-auto px-0">
        <div class="text-center mb-16 relative z-30  animate-fade-down">
            <h1 class="text-4xl md:text-6xl font-semibold text-white mb-6">
                Our Record
            </h1>
            <p class="text-lg md:text-2xl text-gray-200 max-w-2xl mx-auto leading-relaxed">
                A journey of excellence, innovation, and continuous growth in the renowned FIRST® Tech Challenge robotics competition.
            </p>
        </div>

        <div class="relative mx-auto animate-fade">
          <div class="hidden lg:block absolute left-[calc(theme(spacing.10))] md:left-1/2 transform md:-translate-x-1/2 w-8 h-8 bg-green-400 rounded-full border-4 border-gray-900 z-10 bottom-0"></div>
            <div class="hidden lg:block absolute left-[calc(theme(spacing.12))] md:left-1/2 transform md:-translate-x-1/2 w-1 h-full bg-gradient-to-b from-yellow-400 via-blue-400 to-green-400 rounded-full"></div>

            {#each seasons as season, i}
                <div class="relative mb-16">
                    <div class="hidden lg:block absolute left-[calc(theme(spacing.10))] md:left-1/2 transform md:-translate-x-1/2 w-8 h-8 {season.nodeColor} rounded-full border-4 border-gray-900 z-10"></div>
                    
                    <div class="flex items-center gap-8 ">
                        {#if i === 0}
                            <div class="hidden lg:flex flex-1 justify-center items-center">
                                <div class="slideshow-carousel">
                                    {#each carouselImages1 as image, idx}
                                        <img 
                                            src={image} 
                                            alt="Undefined Robotics 2024-25 Season Competition Photo {idx + 1}" 
                                            class="slideshow-image"
                                            class:active={idx === currentIndex1}
                                        />
                                    {/each}
                                </div>
                            </div>
                        {/if}

                        <div 
                            class="flex justify-start flex-1"
                            class:md:justify-end={i % 2 === 0}
                            class:md:pr-12={i % 2 === 0}
                            class:md:pl-12={i % 2 !== 0}
                        >
                            <div class="w-full md:w-[45rem] bg-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10 hover:bg-white/10 transition-all duration-300">
                            <div class="inline-block {season.badgeTextColor} px-4 py-2 rounded-full font-bold text-lg mb-6" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
                                🏆 {season.year}
                            </div>
                            
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-6 md:auto-rows-fr">
                                {#each season.awards as award}
                                    <div class="flex items-start space-x-4">
                                        <div class="w-3 h-3 {award.color} rounded-full mt-2 flex-shrink-0"></div>
                                        <div class="flex-1">
                                            <h3 class="text-xl font-bold text-white mb-2">{award.title}</h3>
                                            {#each award.locations as location}
                                                <p class="text-gray-300 text-sm">{location}</p>
                                            {/each}
                                        </div>
                                    </div>
                                {/each}
                            </div>
                            </div>
                        </div>

                        {#if i === 1}
                            <div class="hidden lg:flex flex-1 justify-center items-center">
                                <div class="slideshow-carousel">
                                    {#each carouselImages2 as image, idx}
                                        <img 
                                            src={image} 
                                            alt="Undefined Robotics 2023-24 Season Competition Photo {idx + 1}" 
                                            class="slideshow-image"
                                            class:active={idx === currentIndex2}
                                        />
                                    {/each}
                                </div>
                            </div>
                        {/if}
                    </div>
                </div>
            {/each}

        </div>
    </div>


    <div class="flex justify-center ">
      <div class="border-t border-white/20 pt-16 max-w-7xl">
        <div class=" animate-fade-up">
        <div class="text-center mb-12">
          <h2 class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-400 to-yellow-100 bg-clip-text text-transparent mb-4">
            The Next Step
          </h2>
          <p class="text-lg text-gray-300 max-w-2xl mx-auto">
            Building on our success, we're expanding our mission to create lasting impact in robotics/STEM education and community development.
          </p>
        </div>
  
  
  
        <div class="mb-12">
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10 max-w-3xl mx-auto">
            <h3 class="text-2xl font-bold text-white mb-6 text-center">Our Roadmap</h3>
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="w-3 h-3 bg-green-400 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <h4 class="text-lg font-semibold text-white mb-2">Continue local events</h4>
                  <p class="text-gray-300">Maintain our commitment to local community engagement and mentorship</p>
                </div>
              </div>
              <div class="flex items-start space-x-4">
                <div class="w-3 h-3 bg-blue-400 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <h4 class="text-lg font-semibold text-white mb-2">Expand our reach (global connections)</h4>
                  <p class="text-gray-300">Establish partnerships with international organizations and schools</p>
                </div>
              </div>
              <div class="flex items-start space-x-4">
                <div class="w-3 h-3 bg-yellow-400 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <h4 class="text-lg font-semibold text-white mb-2">Have successful FTC (Robotics) season</h4>
                  <p class="text-gray-300">Continue our competitive excellence while mentoring the next generation</p>
                </div>
              </div>
            </div>
          </div>
        </div>
  
        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold bg-gradient-to-r to-white from-blue-400 bg-clip-text text-transparent mb-2">Connect</h3>
            <p class="text-gray-300 text-sm">Connecting and establishing partnerships with other local non-profit projects</p>
          </div>
          
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold bg-gradient-to-r to-white from-green-400 bg-clip-text text-transparent mb-2">Empower</h3>
            <p class="text-gray-300 text-sm">Connecting with and teaching adoption centers and schools of underrepresented around the globe</p>
          </div>
          
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-yellow-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold bg-gradient-to-r to-white from-yellow-400 bg-clip-text text-transparent mb-2">Repeat</h3>
            <p class="text-gray-300 text-sm">Raise money and partnerships to teach senior citizens about robotics and digital literacy</p>
          </div>
          
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-purple-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold bg-gradient-to-r to-white from-purple-400 bg-clip-text text-transparent mb-2">Share</h3>
            <p class="text-gray-300 text-sm">Continue mentoring, being involved in, and inspiring the future of local to global communities</p>
          </div>
        </div>
      </div>
      </div>

      
    </div>
    
    <div class="max-w-7xl mx-auto px-6 md:px-8 lg:px-10 py-16 relative z-30">
      <div class="border-t border-white/20 pt-16">
        <div class="animate-fade">
        <div class="text-center mb-12 ">
          <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">
            Fundraising Overview
          </h2>
          <p class="text-lg text-gray-300 max-w-2xl mx-auto mb-6">
            Fiscally sponsored by the <a href="https://the.hackfoundation.org/" target="_blank" rel="noopener noreferrer" class="underline hover:text-yellow-400">Hack Foundation</a>, the Undefined Robotics Non Profit Project is working with <a href="https://app.candid.org/profile/16402866/undefined-robotics" target="_blank" rel="noopener noreferrer" class="underline hover:text-yellow-400">Candid</a> to deliver full transparency to everyone and has been unofficially verified for the Platinum Seal*.
          </p>
          <p class="text-sm text-gray-400 max-w-2xl mx-auto">
            * We are one of the first few HCB fiscally sponsored projects to make a profile under Candid and among the very few first to be unofficially verified for the Platinum Seal by the Candid Director of Partnerships. Public facing seals for FSPs will start rolling out early 2026 (our FSP will be one of the first to receive).
          </p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-6">
          <a href={irsLetter} target="_blank" rel="noopener noreferrer" class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300 group">
            <div class="flex items-center justify-center mb-4">
              <svg class="w-16 h-16 text-yellow-400 group-hover:scale-110 transition-transform duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 text-center">IRS 501(c)(3) Letter</h3>
            <p class="text-gray-300 text-sm text-center">Official tax-exempt status determination letter</p>
          </a>
          
          <a href={certificateOfStatus} target="_blank" rel="noopener noreferrer" class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300 group">
            <div class="flex items-center justify-center mb-4">
              <svg class="w-16 h-16 text-blue-400 group-hover:scale-110 transition-transform duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 text-center">Certificate of Status</h3>
            <p class="text-gray-300 text-sm text-center">Official state registration certificate</p>
          </a>
          
          <a href={fiscalSponsorshipLetter} target="_blank" rel="noopener noreferrer" class="bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300 group">
            <div class="flex items-center justify-center mb-4">
              <svg class="w-16 h-16 text-green-400 group-hover:scale-110 transition-transform duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-white mb-2 text-center">Fiscal Sponsorship Letter</h3>
            <p class="text-gray-300 text-sm text-center">Fiscal sponsorship agreement documentation</p>
          </a>
        </div>

        </div>
      </div>
    </div>
</section>