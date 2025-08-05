
<script>
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
      sticker




    };
    
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
              
   <div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-20">
  <div class="text-center">
    <div class="text-3xl md:text-4xl font-bold text-yellow-400 mb-2">$25K+</div>
    <div class="text-gray-300">Value Raised</div>
  </div>
  <div class="text-center">
    <div class="text-3xl md:text-4xl font-bold text-yellow-400 mb-2">4,000+</div>
    <div class="text-gray-300">Underserved Individuals Reached</div>
  </div>
  <div class="text-center">
    <div class="text-3xl md:text-4xl font-bold text-yellow-400 mb-2">36+</div>
    <div class="text-gray-300">FTC Teams Supported</div>
  </div>
  <div class="text-center">
    <div class="text-3xl md:text-4xl font-bold text-yellow-400 mb-2">10+</div>
    <div class="text-gray-300">Regional/National Awards</div>
  </div>
</div>

  
      <div class="space-y-16">
        
        <div class="bg-white/5 backdrop-blur-sm rounded-xl overflow-hidden border border-white/10">
          <div class="relative bg-cover bg-center h-32" style="background-image: url({images.mentorshipBanner});">
            <div class="absolute inset-0 bg-gradient-to-r from-yellow-900/80 to-yellow-800/60"></div>
            <div class="relative h-full flex items-center justify-center">
              <h3 class="text-3xl font-bold text-yellow-100">Mentorship</h3>
            </div>
          </div>
          
          
          <div class="p-8">
            <div class="grid md:grid-cols-3 gap-6">
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.three} alt="3D" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">3D Print Showcase</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Organized a multi-location STEM outreach event across North Texas. Distributed over 200 eco-friendly 3D-printed robots to families in malls and parks. Engaged professionals from Tesla and Amazon to spark STEM dialogue.</p>
                  </div>
                  <div>
                    <div class="text-sm text-yellow-300 font-semibold">Impact:</div>
                    <div class="text-sm text-yellow-300 font-semibold">Engaged 500+ families in STEM</div>
                    <div class="text-sm text-yellow-300 font-semibold">Distributed 200+ 3D-printed robots</div>
                  </div>
                </div>
              </div>
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.smart} alt="Smart Seniors!" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Smart Seniors (Video Series)</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Partnered with Solace Global to teach senior citizens about online safety through an accessible video series focused on phishing, scams, and fraud prevention.</p>
                  </div>
                  <div>
                    <div class="text-sm text-blue-300 font-semibold">Impact:</div>
                    <div class="text-sm text-blue-300 font-semibold">Educated 300+ seniors</div>
                    <div class="text-sm text-blue-300 font-semibold">Created video series to increase digital literacy</div>
                  </div>
                </div>
              </div>
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.env} alt="Enviromental Workshop" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Enviormental Workshop</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Hosted a hands-on workshop in collaboration with Solace Global to demonstrate how robotics can help tackle environmental issues like waste and renewable energy.</p>
                  </div>
                  <div>
                    <div class="text-sm text-green-300 font-semibold">Impact:</div>
                    <div class="text-sm text-green-300 font-semibold">Taught 20+ students about robotics and sustainability</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
  

  
        <div class="bg-white/5 backdrop-blur-sm rounded-xl overflow-hidden border border-white/10">
          <div class="relative bg-cover bg-center h-32" style="background-image: url({images.communityBanner});">
            <div class="absolute inset-0 bg-gradient-to-r from-blue-900/80 to-blue-800/60"></div>
            <div class="relative h-full flex items-center justify-center">
              <h3 class="text-3xl font-bold text-blue-100">Connecting With the Community</h3>
            </div>
          </div>
          
          <div class="p-8">
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.week} alt="Weekly Coding Classes" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Weekly Girls Coding Classes</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Collaborated with Code.org to host an 8-week beginner-friendly course based on AP Computer Science Principles for girls aged 10–14.</p>
                  </div>
                  <div>
                    <div class="text-sm text-yellow-300 font-semibold">Impact:</div>
                    <div class="text-sm text-yellow-300 font-semibold">Introduced 50+ girls to coding</div>
                    <div class="text-sm text-yellow-300 font-semibold">Built multiple real-world applications</div>
                  </div>
                </div>
              </div>
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.career} alt="Career" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Career Literacy Program</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Created 25+ career videos with Solace Global showcasing real-world engineering disciplines. Each video averaged 2,000 views, broadening access to STEM guidance.</p>
                  </div>
                  <div>
                    <div class="text-sm text-blue-300 font-semibold">Impact:</div>
                    <div class="text-sm text-blue-300 font-semibold">Produced 25+ career videos</div>
                    <div class="text-sm text-blue-300 font-semibold">Each received ~2,000 views</div>
                  </div>
                </div>
              </div>
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.tribe} alt="Career" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Spreading First in South Asia</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Worked with Janajati Ashram and StepsToDo to introduce tribal children in rural India to STEM via hands-on windmill building and renewable energy concepts.</p>
                  </div>
                  <div>
                    <div class="text-sm text-green-300 font-semibold">Impact:</div>
                    <div class="text-sm text-green-300 font-semibold">Empowered 40+ tribal children</div>
                    <div class="text-sm text-green-300 font-semibold">Donated ₹10,000 in STEM supplies</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
  
  
        <div class="bg-white/5 backdrop-blur-sm rounded-xl overflow-hidden border border-white/10">
          <div class="relative bg-cover bg-center h-32" style="background-image: url({images.inspiringBanner});">
            <div class="absolute inset-0 bg-gradient-to-r from-purple-900/80 to-purple-800/60"></div>
            <div class="relative h-full flex items-center justify-center">
              <h3 class="text-3xl font-bold text-purple-100">Motivating the Future</h3>
            </div>
          </div>
          
           <div class="p-8">
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.int} alt="International Girls Robotics " class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">International Girl Robotics</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Partnered with Naihati New Life Society, West India’s largest orphanage for girls affected by abuse, to donate EV3 and SPIKE Prime kits and host robotics/STEM workshops.</p>
                  </div>
                  <div>
                    <div class="text-sm text-yellow-300 font-semibold">Impact:</div>
                    <div class="text-sm text-yellow-300 font-semibold">Reached 15+ abuse survivors</div>
                    <div class="text-sm text-yellow-300 font-semibold">Donated $3,000 in robotics kits</div>
                  </div>
                </div>
              </div>
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.climate} alt="Career" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Robotics for Climate Change</h4>
                    </div>
                    <p class="text-gray-300 mb-4">With a UTD researcher, taught students in grades 1–6 how to build and program SPARK PRIME robots for climate-related challenges. The project gained viral reach.
</p>
                  </div>
                  <div>
                    <div class="text-sm text-blue-300 font-semibold">Impact:</div>
                    <div class="text-sm text-blue-300 font-semibold">Introduced 15+ young students to STEM</div>
                    <div class="text-sm text-blue-300 font-semibold">Earned 6,000+ TikTok views</div>
                  </div>
                </div>
              </div>
              <div class="impact-card flex flex-col bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <img src={images.sticker} alt="Sticker" class="w-full h-40 object-cover rounded-md mb-4" style="min-height:10rem; max-height:10rem;" />
                <div class="flex-1 flex flex-col justify-between">
                  <div>
                    <div class="flex items-center mb-4">
                      <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
                      <h4 class="text-xl font-semibold text-white">Promoted FTC at TEDx Event</h4>
                    </div>
                    <p class="text-gray-300 mb-4">Represented and promoted the FIRST Tech Challenge program at a TEDx Youth event, inspiring attendees to explore robotics and get involved in hands-on STEM learning. Shared personal experiences to break down barriers and encourage participation.

</p>
                  </div>
                  <div>
                    <div class="text-sm text-green-300 font-semibold">Impact:</div>
                    <div class="text-sm text-green-300 font-semibold">Reached diverse TEDx audience with robotics awareness</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
  <div class="mb-16 text-center text-sm text-gray-400 italic px-4">
  Certain events and projects are not displayed as the 25-26 season is in progress.
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