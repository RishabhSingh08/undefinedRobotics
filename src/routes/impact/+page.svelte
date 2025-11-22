<script>
    import StatsGrid from '../../lib/components/StatsGrid.svelte';
    import hero from '../../lib/images/bigImages/1.png';
    import mentorshipBanner from '../../lib/images/bigImages/2.png';
    import communityBanner from '../../lib/images/bigImages/3.png';
    import inspiringBanner from '../../lib/images/bigImages/1.png';
    import three from '../../lib/events/3d.jpg';
    import env from '../../lib/events/env.jpg';
    import smart from '../../lib/events/smart.jpg';
    import week from '../../lib/events/week.jpg';
    import career from '../../lib/events/career.jpg';
    import tribe from '../../lib/events/tribe.jpg';
    import int from '../../lib/events/int.jpg';
    import climate from '../../lib/events/climate.jpg';
    import sticker from '../../lib/events/sticky.jpg';
    import bsl from '../../lib/events/bsl.jpg';
    import mnm from '../../lib/events/mnm.jpg';
    import indhero from '../../lib/events/indhero.jpg';
    import g1 from '../../lib/events/Screenshot 2025-11-09 200540.png';
    export let images = {
      hero,
      mentorshipBanner,
      communityBanner,
      inspiringBanner,
      three,
      env,
      smart,
      week,
      career,
      tribe,
      int,
      climate,
      sticker,
      bsl,
      mnm,
      indhero,
      g1
    };

    const impactSections = [
      {
        title: 'Mentorship',
        banner: mentorshipBanner,
        gradientFrom: 'yellow-900/80',
        gradientTo: 'yellow-800/60',
        textColor: 'yellow-100',
        dotColor: 'yellow-400',
        impactColor: 'yellow-300',
        gridCols: 'md:grid-cols-3',
        events: [
          {
            image: three,
            imageAlt: '3D',
            title: '3D Print Showcase',
            description: 'Organized a multi-location STEM outreach event across North Texas. Distributed over 200 eco-friendly 3D-printed robots to families in malls and parks. Engaged professionals from Tesla and Amazon to spark STEM dialogue.',
            impacts: ['Engaged 500+ families in STEM', 'Distributed 200+ 3D-printed robots']
          },
          {
            image: smart,
            imageAlt: 'Smart Seniors!',
            title: 'Smart Seniors (Video Series)',
            description: 'Taught senior citizens about online safety through an accessible video series focused on phishing, scams, and fraud prevention.',
            impacts: ['Educated 300+ seniors', 'Created video series to increase digital literacy']
          },
          {
            image: env,
            imageAlt: 'Enviromental Workshop',
            title: 'Enviormental Workshop',
            description: 'Hosted a hands-on workshop to demonstrate how robotics can help tackle environmental issues like waste and renewable energy.',
            impacts: ['Taught 20+ students about robotics and sustainability']
          }
        ]
      },
      {
        title: 'Connecting With the Community',
        banner: communityBanner,
        gradientFrom: 'blue-900/80',
        gradientTo: 'blue-800/60',
        textColor: 'blue-100',
        dotColor: 'yellow-400',
        impactColor: 'yellow-300',
        gridCols: 'md:grid-cols-2 lg:grid-cols-3',
        events: [
          {
            image: week,
            imageAlt: 'Weekly Coding Classes',
            title: 'Weekly Girls Coding Classes',
            description: 'Collaborated with Code.org to host an 8-week beginner-friendly course based on AP Computer Science Principles for girls aged 10–14.',
            impacts: ['Introduced 50+ girls to coding', 'Built multiple real-world applications']
          },
          {
            image: career,
            imageAlt: 'Career',
            title: 'Career Literacy Program',
            description: 'Created 25+ career videos showcasing real-world engineering disciplines. Each video averaged 2,000 views, broadening access to STEM guidance.',
            impacts: ['Produced 25+ career videos', 'Each received ~2,000 views']
          },
          {
            image: tribe,
            imageAlt: 'Career',
            title: 'Spreading First in South Asia',
            description: 'Worked with Janajati Ashram and StepsToDo to introduce tribal children in rural India to STEM via hands-on windmill building and renewable energy concepts.',
            impacts: ['Empowered 40+ tribal children', 'Donated ₹10,000 in STEM supplies']
          }
        ]
      },
      {
        title: 'Motivating the Future',
        banner: inspiringBanner,
        gradientFrom: 'purple-900/80',
        gradientTo: 'purple-800/60',
        textColor: 'purple-100',
        dotColor: 'yellow-400',
        impactColor: 'yellow-300',
        gridCols: 'md:grid-cols-3',
        events: [
          {
            image: int,
            imageAlt: 'International Girls Robotics ',
            title: 'International Girl Robotics',
            description: 'Partnered with Naihati New Life Society, West India\'s largest orphanage for girls affected by abuse, to donate EV3 and SPIKE Prime kits and host robotics/STEM workshops.',
            impacts: ['Reached 15+ abuse survivors', 'Donated $3,000 in robotics kits']
          },
          {
            image: climate,
            imageAlt: 'Career',
            title: 'Robotics for Climate Change',
            description: 'With a UTD researcher, taught students in grades 1–6 how to build and program SPARK PRIME robots for climate-related challenges. The project gained viral reach.',
            impacts: ['Introduced 15+ young students to STEM', 'Earned 6,000+ TikTok views']
          },
          {
            image: sticker,
            imageAlt: 'Sticker',
            title: 'Promoted FTC at TEDx Event',
            description: 'Represented and promoted the FIRST Tech Challenge program at a TEDx Youth event, inspiring attendees to explore robotics and get involved in hands-on STEM learning. Shared personal experiences to break down barriers and encourage participation.',
            impacts: ['Reached diverse TEDx audience with robotics awareness'],
            dotColor: '#853dc4',
            impactColor: 'purple-500'
          }
        ]
      },
      {
        title: 'Industry Connections & Insights',
        banner: indhero,
        gradientFrom: 'green-900/80',
        gradientTo: 'green-800/60',
        textColor: 'green-100',
        dotColor: 'green-400',
        impactColor: 'green-300',
        gridCols: 'md:grid-cols-2 lg:grid-cols-3',
        events: [
          {
            image: bsl,
            imageAlt: 'Build Show Live 2025',
            title: 'Build Show Live 2025',
<<<<<<< Updated upstream
            description: 'At Build Show LIVE 2025 in Dallas, our team met industry leaders to discuss robotics, STEM outreach, and how technology can empower future builders.',
=======
<<<<<<< HEAD
            description: 'At Build Show LIVE 2025 in Dallas, the team reached an impact of 5,400 attendees by showcasing an expo robot chassis, live 3D printing demonstrations, and hands-on arm module experiences that highlighted nonprofit outreach and FIRST principles. The event facilitated connections with over 35 industry professionals from 15 Fortune 500 and major tech companies, including senior executives who shared engineering insights that enriched the team\'s technical approach.',
=======
            description: 'At Build Show LIVE 2025 in Dallas, our team met industry leaders to discuss robotics, STEM outreach, and how technology can empower future builders.',
>>>>>>> 8ce84da9c07a1ded52ed0d406bf5e18ceb78c606
>>>>>>> Stashed changes
            impacts: ['Connected students with industry professionals', 'Expanded STEM and robotics outreach network']
          },
          {
            image: mnm,
            imageAlt: 'Mentorship Session with M&M Engineering Supervisor',
            title: 'M&M Engineering Mentorship',
<<<<<<< Updated upstream
            description: 'Team members met with M&M Engineering Supervisor Mr. Neaves to present robot designs, discuss improvements, and gain expert feedback on this year’s challenge.',
            impacts: ['Enhanced robot design through expert feedback', 'Strengthened partnership with M&M Engineering with 5 hour tour and 2 hour review session']
=======
<<<<<<< HEAD
            description: 'Team members engaged in a comprehensive seven-hour collaboration with M&M Engineering Supervisor Mr. Neaves, including a 5+ facility tour and 2+ CAD review session. During this visit, the team presented robot designs, discussed design improvements for this year\'s challenge, and received expert technical feedback that provided valuable insights for optimizing their engineering approach.',
            impacts: ['Enhanced robot design through expert feedback', 'Strengthened partnership with M&M Engineering']
>>>>>>> Stashed changes
          },
          {
            image: g1,
            imageAlt: 'Industry Engagements',
            title: 'Industry Engagements',
            description: 'The team connected with industry leaders across aerospace, manufacturing, and technology sectors, gaining firsthand insights into how robotics and automation are transforming production processes, addressing labor challenges, and driving innovation. These conversations illuminated real-world applications that directly inform and elevate the team\'s STEM projects and technical approach.',
            impacts: [
              'Gained insight into real-world robotics',
              'Built connections with major industry innovators',
            ]
          }
=======
            description: 'Team members met with M&M Engineering Supervisor Mr. Neaves to present robot designs, discuss improvements, and gain expert feedback on this year’s challenge.',
            impacts: ['Enhanced robot design through expert feedback', 'Strengthened partnership with M&M Engineering with 5 hour tour and 2 hour review session']
          },
{
  image: g1,
  imageAlt: 'Industry Engagements',
  title: 'Industry Engagements',
  description: 'Our team met leaders from aerospace, manufacturing, and tech sectors, learning how robotics and automation drive modern industries and inspire our own STEM work.',
  impacts: [
    'Gained insight into real-world robotics',
    'Connected with 15 Fortune 500 companies to learn engineering process',
  ]
}

>>>>>>> 8ce84da9c07a1ded52ed0d406bf5e18ceb78c606
        ]
      }
    ];
    
  </script>
  
  <section id="impact" class="px-4 py-32 relative z-10">
    <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>



    <div class="max-w-7xl mx-auto">
      <div class="relative mb-20 rounded-3xl overflow-hidden text-white">
        <img
          src={images.hero}
          alt="Mentorship"
          class="w-full h-[500px] object-cover"
        />
      
        <div class="absolute inset-0 bg-gradient-to-t from-black via-5% to-transparent"></div>
      
        <div class="absolute bottom-0 left-0 w-full px-10 pb-10">
          <h1 class="text-4xl md:text-6xl font-semibold text-white mb-3">
            Our Impact
          </h1>
          <p class="text-lg md:text-2xl text-gray-200 max-w-2xl">
            Transforming communities through robotics education, mentorship, and STEM outreach across the world.
          </p>
        </div>
      </div>
              
   <div class="mb-20 relative z-30">
     <StatsGrid />
   </div>

  <hr
  class="h-px border-t-0 bg-transparent bg-gradient-to-r from-transparent via-neutral-500 to-transparent opacity-25 dark:via-neutral-400" />

        <div class="mt-12 mb-20 text-center relative z-20">
          <div class="inline-flex items-center justify-center gap-4">
            <h2 class="text-5xl md:text-7xl font-semibold tracking-wide text-white">
              Top Events
            </h2>
          </div>
          <div class="flex justify-center mt-8">
            <div class="flex flex-col md:flex-row justify-center gap-4 md:gap-8 max-w-3xl">
  
              <div class="flex items-center justify-center md:justify-start">
                <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                <h4 class="text-lg md:text-xl font-semibold text-white">Undefined #25782</h4>
              </div>
  
              <div class="flex items-center justify-center md:justify-start">
                <div class="w-3 h-3 bg-[#853dc4] rounded-full mr-3"></div>
                <h4 class="text-lg md:text-xl font-semibold text-white">Missing Amps #30801</h4>
              </div>
            </div>
          </div>
        </div>
          
            <div class="space-y-16">
        {#each impactSections as section}
          <div class="bg-white/5 backdrop-blur-sm rounded-xl overflow-hidden border border-white/10">
            <div class="relative bg-cover bg-center h-32" style="background-image: url({section.banner});">
              {#if section.title === 'Mentorship'}
                <div class="absolute inset-0 bg-gradient-to-r from-yellow-900/80 to-yellow-800/60"></div>
                <div class="relative h-full flex items-center justify-center px-4">
                  <h3 class="text-2xl md:text-3xl font-bold text-yellow-100 text-center">{section.title}</h3>
                </div>
              {:else if section.title === 'Connecting With the Community'}
                <div class="absolute inset-0 bg-gradient-to-r from-blue-900/80 to-blue-800/60"></div>
                <div class="relative h-full flex items-center justify-center px-4">
                  <h3 class="text-2xl md:text-3xl font-bold text-blue-100 text-center">{section.title}</h3>
                </div>
              {:else if section.title === 'Industry Connections & Insights'}
                <div class="absolute inset-0 bg-gradient-to-r from-green-900/80 to-green-800/60"></div>
                <div class="relative h-full flex items-center justify-center px-4">
                  <h3 class="text-2xl md:text-3xl font-bold text-green-100 text-center">{section.title}</h3>
                </div>
              {:else}
                <div class="absolute inset-0 bg-gradient-to-r from-purple-900/80 to-purple-800/60"></div>
                <div class="relative h-full flex items-center justify-center px-4">
                  <h3 class="text-2xl md:text-3xl font-bold text-purple-100 text-center">{section.title}</h3>
                </div>
              {/if}
            </div>
            
            <div class="p-8">
              <div class="grid {section.gridCols} gap-6">
                {#each section.events as event}
                  <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                    <img src={event.image} alt={event.imageAlt} class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                    <div class="flex-1 flex flex-col justify-between">
                      <div>
                        <div class="flex items-center mb-4">
                          {#if event.dotColor}
                            <div class="w-3 h-3 rounded-full mr-3" style="background-color: {event.dotColor}"></div>
                          {:else}
                            <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                          {/if}
                          <h4 class="text-xl font-semibold text-white">{event.title}</h4>
                        </div>
                        <p class="text-gray-300 mb-4">{event.description}</p>
                      </div>
                      <div>
                        <p class="font-medium" style="background: linear-gradient(to right, {event.dotColor || '#facc15'}, {event.dotColor ? `${event.dotColor}cc` : '#fde68a'}); -webkit-background-clip: text; -webkit-text-fill-color: transparent; display: inline-block">Impact</p>
                        <div class="space-y-1">
                          {#each event.impacts as impact}
                            <div class="text-sm text-gray-400">
                              - {impact}
                            </div>
                          {/each}
                        </div>
                      </div>
                    </div>
                  </div>
                {/each}
              </div>
            </div>
          </div>
        {/each}
  <div class="text-center text-sm text-gray-400 italic px-4">
  Certain events and programs/initiatives are not displayed for confidentiality through the 25-26 season.
</div>


  
      </div>
    </div>
  </section>

  <style>
  .impact-card {
    min-height: 420px;
    height: 100%;
  }
  </style>