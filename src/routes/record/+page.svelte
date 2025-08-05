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
                            <div class="inline-block {season.badgeBgColor} {season.badgeTextColor} px-4 py-2 rounded-full font-bold text-lg mb-6">
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
</section>

<style>
</style>