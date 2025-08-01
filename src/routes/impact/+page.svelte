
<script>
    import hero from '../../lib/images/bigImages/1.png';
    import mentorshipBanner from '../../lib/images/bigImages/2.png';
    import communityBanner from '../../lib/images/bigImages/3.png';
    import inspiringBanner from '../../lib/images/bigImages/1.png';

    export let images = {
      hero,
      mentorshipBanner,
      communityBanner,
      inspiringBanner,
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
    <div class="text-3xl md:text-4xl font-bold text-yellow-400 mb-2">$50K+</div>
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
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Ravenclaw Robotics</h4>
                </div>
                <p class="text-gray-300 mb-4">Helped our feeder school FTC team via assisting in the development of their robot and developing competition strategies.</p>
                <div class="text-sm text-blue-300 font-semibold">Impact: 6 FTC Teams, 70 People</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Senior Team Partnership</h4>
                </div>
                <p class="text-gray-300 mb-4">Senior teams greatly helped employ our designs and functionality, forming the pillars of our success. Notable contributors include Plano West HS and the Association of Chinese Professionals (ACP).</p>
                <div class="text-sm text-green-300 font-semibold">Impact: 30+ Students</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-purple-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Evan Mead of UTD</h4>
                </div>
                <p class="text-gray-300 mb-4">Evan Mead is an FTC alumni currently studying at UTD and kickstarted our 2022 season with valuable insights on robot design.</p>
                <div class="text-sm text-purple-300 font-semibold">Impact: Team Development</div>
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
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Scrimmage Hosting</h4>
                </div>
                <p class="text-gray-300 mb-4">Hosted scrimmage at our school with 6 local teams, providing some teams their first opportunity to use a full practice field and run real matches.</p>
                <div class="text-sm text-yellow-300 font-semibold">Impact: 6 FTC Teams</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">League Tournament Hosting</h4>
                </div>
                <p class="text-gray-300 mb-4">Hosted the FIRST in Texas E&F League Tournament in our school which provided a platform for 30+ teams to compete in the qualifying/knockout stages of the FIRST Tech Challenge championship.</p>
                <div class="text-sm text-blue-300 font-semibold">Impact: 30+ FTC Teams, 800+ people</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Tech the Halls</h4>
                </div>
                <p class="text-gray-300 mb-4">Winter collaboration event with other school-centric STEM organizations that taught students the fundamentals of the Engineering Design Process via interactive engineering, CAD modeling, and coding workshops.</p>
                <div class="text-sm text-green-300 font-semibold">Impact: 2000+ Students</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-purple-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">FIRST Seminar</h4>
                </div>
                <p class="text-gray-300 mb-4">Partnered with accomplished FTC teams and notable alumni in conducting a seminar on the impact of the FIRST organization and incentivized participants to spread STEM learning.</p>
                <div class="text-sm text-purple-300 font-semibold">Impact: Jasper HS students, 90 people in-person, 20+ online viewers</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">PISD Robotics Demo</h4>
                </div>
                <p class="text-gray-300 mb-4">Advocated for improving upon STEM application at our school and showcased the application of STEM education to district admins by building and programming robots to incentivize increased funding, resources, and reach.</p>
                <div class="text-sm text-yellow-300 font-semibold">Impact: School Administrators</div>
              </div>
  
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-red-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Annual School Pep Rally</h4>
                </div>
                <p class="text-gray-300 mb-4">Featured our robot and team while conveying FIRST and STEM ideals at Jasper HS Spring Pep Rally which all students and staff attend. The day of the event is dedicated to showcasing our robot and giving opportunities for others to be involved.</p>
                <div class="text-sm text-red-300 font-semibold">Impact: Jasper HS staff and student body</div>
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
            <div class="grid md:grid-cols-2 lg:grid-cols-2 gap-6">
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-blue-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Coding Camps</h4>
                </div>
                <p class="text-gray-300 mb-4">Partnered with UTD grads to teach students under 13 Java programming via interactive meetings and informative activities.</p>
                <div class="text-sm text-blue-300 font-semibold">Impact: 10 people</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-green-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">What is Robotics?</h4>
                </div>
                <p class="text-gray-300 mb-4">Discussed the basics of robotics and its significance to 4th-grade students and helped establish a full-time FIRST Lego League team.</p>
                <div class="text-sm text-green-300 font-semibold">Impact: 1 FLL Team Established</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-yellow-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Intro to FTC</h4>
                </div>
                <p class="text-gray-300 mb-4">Introduced FTC to the Robinson FLL team as a step up and encouraged involvement in the FTC Jasper Robotics community.</p>
                <div class="text-sm text-yellow-300 font-semibold">Impact: 2 Teams Transitioned</div>
              </div>
              
              <div class="bg-white/10 backdrop-blur-sm rounded-lg p-6 border border-white/20 hover:bg-white/15 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-3 h-3 bg-red-400 rounded-full mr-3"></div>
                  <h4 class="text-xl font-semibold text-white">Annual 8th Grade Night</h4>
                </div>
                <p class="text-gray-300 mb-4">Showcased the Jasper robotics program to upcoming 8th graders from our feeder middle schools and highlighted its impacts on the community (~1500 students over the course of two years).</p>
                <div class="text-sm text-red-300 font-semibold">Impact: 1,500+ Students</div>
              </div>
            </div>
          </div>
        </div>
  <div class="mb-16 text-center text-sm text-gray-400 italic px-4">
  Some events are not shown, as our current season is still in progress and many projects are confidential until revealed.
</div>


  
      </div>
    </div>
  </section>

  <style>

  </style>