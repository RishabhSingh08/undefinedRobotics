<script>
    // All your timeline data is now in this single array of objects.
    // To add, remove, or change awards, you only need to edit this data structure.
    const seasons = [
        {
            year: '2024–25 Season',
            nodeColor: 'bg-yellow-400', // Color for the large circle on the timeline
            badgeBgColor: 'bg-yellow-400',
            badgeTextColor: 'text-gray-900',
            awards: [
                {
                    title: 'Control Award',
                    color: 'bg-violet-400', // Color for the small dot next to the award
                    locations: ['FiT-North Area Championship – Stage Left']
                },
                {
                    title: 'RTX Innovate Award',
                    color: 'bg-cyan-400',
                    locations: ['FiT-North Area Championship – Stage Left']
                },
                {
                    title: 'Connect Award',
                    color: 'bg-rose-400',
                    locations: ['Texas FTC Championship – Sapphire Division']
                },
                {
                    title: 'Finalist Alliance Captain',
                    color: 'bg-lime-400',
                    locations: ['Texas FTC Championship – Sapphire Division']
                },
                {
                    title: 'Winning Alliance',
                    color: 'bg-orange-400',
                    locations: ['FiT-North Area Championship – Stage Left']
                }
            ]
        },
        {
            year: '2023–24 Season',
            nodeColor: 'bg-blue-400',
            badgeBgColor: 'bg-blue-400',
            badgeTextColor: 'text-gray-900',
            awards: [
                {
                    title: 'Control Award – 2×',
                    color: 'bg-violet-400',
                    locations: ['FiT-North E&F Tournament', 'FiT-North Area Championship']
                },
                {
                    title: 'Design Award – 2×',
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
                    locations: ['FiT-North Semi-Area Championship (Stage Right)']
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

<section id="record" class="px-4 py-32 relative z-10 min-h-screen">
    <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

    <div class="max-w-[115rem] mx-auto">
        <div class="text-center mb-16">
            <h1 class="text-4xl md:text-6xl font-semibold text-white mb-6">
                Our Record
            </h1>
            <p class="text-lg md:text-2xl text-gray-200 max-w-2xl mx-auto leading-relaxed">
                A journey of excellence, innovation, and continuous growth in the renowned FIRST® Tech Challenge robotics competition.
            </p>
        </div>

        <div class="relative mx-auto">
          <div class=" hidden lg:block absolute left-4 md:left-1/2 transform md:-translate-x-1/2 w-8 h-8 bg-green-400 rounded-full border-4 border-gray-900 z-10 bottom-0"></div>
            <div class=" hidden lg:block absolute left-6 md:left-1/2 transform md:-translate-x-1/2 w-1 h-full bg-gradient-to-b from-yellow-400 via-blue-400 to-green-400 rounded-full"></div>

            {#each seasons as season, i}
                <div class="relative mb-16">
                    <div class="hidden lg:block absolute left-4 md:left-1/2 transform md:-translate-x-1/2 w-8 h-8 {season.nodeColor} rounded-full border-4 border-gray-900 z-10"></div>
                    
                    <div 
                        class="flex justify-start"
                        class:md:justify-end={i % 2 === 0}
                        class:md:pr-12={i % 2 === 0}
                        class:md:pl-12={i % 2 !== 0}
                    >
                        <div class="w-full md:w-[45rem] bg-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10 hover:bg-white/10 transition-all duration-300">
                            <div class="inline-block {season.badgeTextColor} px-4 py-2 rounded-full font-bold text-lg mb-6" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
                                🏆 {season.year}
                            </div>
                            
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                {#each season.awards as award}
                                    <div class="flex items-start space-x-4">
                                        <div class="w-3 h-3 {award.color} rounded-full mt-2 flex-shrink-0"></div>
                                        <div>
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
                </div>
            {/each}

        </div>
    </div>


    <div class="flex justify-center">
      <div class="border-t border-white/20 pt-16 max-w-7xl">
        <div class="text-center mb-12">
          <h2 class="text-3xl md:text-4xl font-bold text-green-300 mb-4">
            The Next Step
          </h2>
          <p class="text-lg text-gray-300 max-w-2xl mx-auto">
            Building on our success, we're expanding our mission to create lasting impact in robotics/STEM education and community development.
          </p>
        </div>
  
  
  
        <div class="mb-12">
          <div class="text-center mb-8">
            <div class="inline-block text-gray-900 px-6 py-3 rounded-full font-bold text-xl mb-4" style="background: linear-gradient(135deg, #ffe281 0%, #ffb63c 100%);">
              2024-25
            </div>
          </div>
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
            <h3 class="text-xl font-bold text-blue-300 mb-2">Connect</h3>
            <p class="text-gray-300 text-sm">Connecting and establishing partnerships with other local non-profit organizations</p>
          </div>
          
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold text-green-300 mb-2">Empower</h3>
            <p class="text-gray-300 text-sm">Connecting with and teaching adoption centers and schools of underrepresented around the globe</p>
          </div>
          
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-yellow-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold text-yellow-300 mb-2">Repeat</h3>
            <p class="text-gray-300 text-sm">Raise money and partnerships to teach senior citizens about robotics and digital literacy</p>
          </div>
          
          <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 text-center hover:bg-white/10 transition-all duration-300">
            <div class="w-16 h-16 bg-purple-500 rounded-full flex items-center justify-center mx-auto mb-4">
              <div class="w-8 h-8 bg-white rounded-full"></div>
            </div>
            <h3 class="text-xl font-bold text-purple-300 mb-2">Share</h3>
            <p class="text-gray-300 text-sm">Continue mentoring, being involved in, and inspiring the future of local to global communities</p>
          </div>
        </div>
      </div>
    </div>
    

    
</section>

<style>
</style>
