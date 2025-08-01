<script>
  import IconLogo from "../../lib/images/logo.png";
  
  let activeTab = 'undefined';

  const undefinedTeamMembers = [
    {
      name: "Akshat Kumar",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano Senior High School",
      image: "https://www.undefinedrobotics.org/akshat_kumar.png"
    },
    {
      name: "Neel M",
      grade: "11th Grade",
      role: "Engineer",
      school: "Plano Senior High School",
      image: "https://www.undefinedrobotics.org/akshat_kumar.png"
    },
    {
      name: "Rishabh Singh",
      grade: "11th Grade",
      role: "Chief Technical Officer",
      school: "Plano Senior High School",
      image: "https://www.undefinedrobotics.org/akshat_kumar.png"
    },
    {
      name: "Punit Lakhotiya",
      grade: "11th Grade",
      role: "Finance/Team Management/Engineer",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/punit_lakhotiya.png"
    },
    {
      name: "Aarav G",
      grade: "11th Grade",
      role: "Outreach",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/punit_lakhotiya.png"
    },
    {
      name: "Navin Rao",
      grade: "11th Grade",
      role: "CAD Modeler/Engineer",
      school: "Plano Senior High School",
      image: "https://www.undefinedrobotics.org/navin_rao.png"
    },
    {
      name: "Lucas Silva",
      grade: "11th Grade",
      role: "Engineer/Driver",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/lucas_silva.png"
    },
    {
      name: "Swaraj Nibandhe",
      grade: "11th Grade",
      role: "Engineer/Team Lead",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/swaraj_nibandhe.png"
    },
    {
      name: "Xander Kuksov",
      grade: "11th Grade",
      role: "Programmer",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/xander_kuksov.png"
    },
    {
      name: "Samanyu Earna",
      grade: "11th Grade",
      role: "Programmer",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/samanyu_earna.png"
    },
    {
      name: "Azalea Tang",
      grade: "11th Grade",
      role: "Programmer",
      school: "Texas Academy of Math and Science",
      image: "https://www.undefinedrobotics.org/azalea_tang.png"
    },
    {
      name: "Ainesh Gupta",
      grade: "11th Grade",
      role: "Engineer",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/ainesh_gupta.png"
    },
    {
      name: "Erik Wang",
      grade: "11th Grade",
      role: "Engineer/Outreach/Driver",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/erik_wang.png"
    },
    {
      name: "Mahit Cherku",
      grade: "11th Grade",
      role: "Outreach/Engineer",
      school: "Memorial High School",
      image: "https://www.undefinedrobotics.org/mahit_cherku.png"
    },
    {
      name: "Vedant Teware",
      grade: "11th Grade",
      role: "Outreach/Engineer",
      school: "Lone Star High School",
      image: "https://www.undefinedrobotics.org/vedant_teware.png"
    },
    {
      name: "Ashwin Gupta",
      grade: "11th Grade",
      role: "Engineer",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/ashwin_gupta.png"
    },
    {
      name: "Nishant Sinari",
      grade: "11th Grade",
      role: "Outreach/CAD Lead",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/nishant_sinari.png"
    },
    {
      name: "Shriya Mohan",
      grade: "11th Grade",
      role: "Outreach",
      school: "Plano Senior High School",
      image: "https://www.undefinedrobotics.org/shriya_mohan.png"
    },
    {
      name: "Darrien Kwan",
      grade: "11th Grade",
      role: "Outreach",
      school: "Plano West Senior High School",
      image: "https://www.undefinedrobotics.org/darrien_kwan.png"
    }
  ];

  // Dummy data for Missing Amps team
  const missingAmpsMembers = [
    {
      name: "Sarah Chen",
      grade: "12th Grade",
      role: "Captain/Electrical Lead",
      school: "Plano East Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=SC"
    },
    {
      name: "Marcus Thompson",
      grade: "11th Grade",
      role: "Co-Captain/Programmer",
      school: "Plano Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=MT"
    },
    {
      name: "Isabella Rodriguez",
      grade: "11th Grade",
      role: "Chief Designer/CAD",
      school: "Plano West Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=IR"
    },
    {
      name: "James Park",
      grade: "10th Grade",
      role: "Engineer/Driver",
      school: "Plano East Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=JP"
    },
    {
      name: "Maya Patel",
      grade: "11th Grade",
      role: "Programmer/Controls",
      school: "Clark High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=MP"
    },
    {
      name: "Tyler Johnson",
      grade: "11th Grade",
      role: "Build Team Lead",
      school: "Plano Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=TJ"
    },
    {
      name: "Sophia Kim",
      grade: "10th Grade",
      role: "Outreach/Marketing",
      school: "Plano West Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=SK"
    },
    {
      name: "Daniel Garcia",
      grade: "11th Grade",
      role: "Engineer/Fabrication",
      school: "Legacy High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=DG"
    },
    {
      name: "Emma Wilson",
      grade: "10th Grade",
      role: "Programmer/Vision",
      school: "Plano East Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=EW"
    },
    {
      name: "Ryan Martinez",
      grade: "11th Grade",
      role: "Scout/Strategy",
      school: "Plano Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=RM"
    },
    {
      name: "Olivia Chang",
      grade: "10th Grade",
      role: "CAD/Design",
      school: "Jasper High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=OC"
    },
    {
      name: "Alex Turner",
      grade: "11th Grade",
      role: "Engineer/Testing",
      school: "Plano West Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=AT"
    },
    {
      name: "Grace Liu",
      grade: "10th Grade",
      role: "Finance/Fundraising",
      school: "Allen High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=GL"
    },
    {
      name: "Ethan Davis",
      grade: "11th Grade",
      role: "Engineer/Assembly",
      school: "Plano East Senior High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=ED"
    },
    {
      name: "Zoe Anderson",
      grade: "10th Grade",
      role: "Media/Documentation",
      school: "Frisco High School",
      image: "https://via.placeholder.com/300x300/3B82F6/FFFFFF?text=ZA"
    }
  ];

  // Chiefs (specified names)
  const chiefNames = ["Akshat Kumar", "Rishabh Singh", "Punit Lakhotiya", "Neel M", "Aarav G"];
  const chiefs = undefinedTeamMembers.filter(member => chiefNames.includes(member.name));

  // Non-chief members for Undefined Robotics
  const undefinedNonChiefs = undefinedTeamMembers.filter(member => !chiefNames.includes(member.name));




</script>

<style>

  
  .tab-active {
    border-bottom: 3px solid #f59e0b;
    color: #f59e0b;
  }
  
  .team-card {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .team-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
  
  .chief-card:hover {
    transform: scale(1.05);
  }
</style>

<main class="px-4 py-32 relative z-10 min-h-screen">
  <!-- Background Effects -->
  <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.1)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>
  <div class="absolute inset-0 z-0">
    <div class="absolute top-0 left-1/4 w-96 h-96 bg-gradient-to-r from-yellow-500 to-yellow-200 rounded-full blur-3xl opacity-10"></div>
    <div class="absolute bottom-0 right-1/4 w-96 h-96 bg-gradient-to-r from-yellow-200 to-yellow-700 rounded-full blur-3xl opacity-10"></div>
  </div>

  <div class="relative z-10 container mx-auto px-6">
    <!-- Header -->
    <div class="text-center mb-16">
      <h1 class="text-4xl md:text-6xl font-semibold text-white mb-6">
        Our Family
      </h1>
      <p class="text-lg md:text-2xl text-gray-200 max-w-2xl mx-auto leading-relaxed">
        Meet the incredible minds driving innovation in robotics across our organization
      </p>
    </div>
    <!-- Chiefs Section -->
    <div class="mb-20">
      <h2 class="text-3xl font-bold text-center mb-12 text-yellow-400">Leadership Team</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-6 max-w-6xl mx-auto">
        {#each chiefs as chief}
          <div class="team-card chief-card bg-gray-900 rounded-xl border border-gray-700 p-6 text-center">
            <div class="w-24 h-24 mx-auto mb-4 rounded-full overflow-hidden bg-gray-700">
              <img 
                src={chief.image} 
                alt={chief.name} 
                class="w-full h-full object-cover"
                on:error={(e) => {
                  e.target.src = `https://via.placeholder.com/96x96/6B7280/FFFFFF?text=${chief.name.split(' ').map(n => n[0]).join('')}`;
                }}
              />
            </div>
            <h3 class="text-lg font-semibold mb-2 text-white">{chief.name}</h3>
            <p class="text-yellow-400 font-medium mb-2 text-sm">{chief.role}</p>
            <p class="text-gray-400 text-sm mb-1">{chief.school}</p>
            <p class="text-gray-500 text-xs">{chief.grade}</p>
          </div>
        {/each}
      </div>
    </div>

    <!-- Team Tabs -->
    <div class="max-w-7xl mx-auto">
      <div class="border-b border-gray-700 mb-8">
        <nav class="flex space-x-8 justify-center">
          <button 
            class="py-4 px-6 text-lg font-semibold transition-colors duration-200"
            class:tab-active={activeTab === 'undefined'}
            class:text-gray-400={activeTab !== 'undefined'}
            class:hover:text-white={activeTab !== 'undefined'}
            on:click={() => activeTab = 'undefined'}
          >
            Undefined Robotics
          </button>

          <button 
            class="py-4 px-6 text-lg font-semibold transition-colors duration-200"
            class:tab-active={activeTab === 'missing'}
            class:text-gray-400={activeTab !== 'missing'}
            class:hover:text-white={activeTab !== 'missing'}
            on:click={() => activeTab = 'missing'}
          >
            Missing Amps
          </button>
        </nav>
      </div>


      <!-- Team Content -->
    {#if activeTab === 'undefined'}
      <div class="team-content">
        <div class="mb-12">
          <div class="w-full h-80 bg-gradient-to-br from-gray-800 to-gray-900 rounded-2xl flex items-center justify-center border border-gray-700">
            <div class="text-center">
              <div class="w-24 h-24 bg-yellow-500 rounded-full mx-auto mb-4 flex items-center justify-center">
                <svg class="w-12 h-12 text-black" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M4 3a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V5a2 2 0 00-2-2H4zm12 12H4l4-8 3 6 2-4 3 6z" clip-rule="evenodd"></path>
                </svg>
              </div>
              <p class="text-gray-400">Team Photo Coming Soon</p>
            </div>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
            <h3 class="text-xl font-bold mb-4 text-yellow-400">Team Information</h3>
            <div class="space-y-3">
              <div><span class="text-gray-400">Team Number:</span> <span class="text-white font-semibold">#2024</span></div>
              <div><span class="text-gray-400">Members:</span> <span class="text-white font-semibold">{undefinedTeamMembers.length} Students</span></div>
              <div><span class="text-gray-400">Coach:</span> <span class="text-white font-semibold">Mr. Johnson</span></div>
              <div><span class="text-gray-400">Founded:</span> <span class="text-white font-semibold">2020</span></div>
              <div><span class="text-gray-400">Competition:</span> <span class="text-white font-semibold">FRC</span></div>
            </div>
          </div>
          
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
            <h3 class="text-xl font-bold mb-4 text-yellow-400">Our Story</h3>
            <p class="text-gray-300 leading-relaxed">
              Undefined Robotics was born from a shared passion for innovation and problem-solving. 
              Our team combines diverse talents in engineering, programming, and design to create 
              cutting-edge robotic solutions. We believe in pushing boundaries and exploring the 
              undefined possibilities of robotics technology.
            </p>
          </div>
        </div>

        <div>
          <h3 class="text-2xl font-bold mb-8 text-center text-yellow-400">Team Members</h3>
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
            {#each undefinedNonChiefs as member}
              <div class="team-card bg-gray-900 rounded-xl border border-gray-700 p-6 text-center hover:border-gray-600 transition-all duration-300">
                <div class="w-20 h-20 mx-auto mb-4 rounded-full overflow-hidden bg-gray-700">
                  <img 
                    src={member.image} 
                    alt={member.name} 
                    class="w-full h-full object-cover"
                    on:error={(e) => {
                      e.target.src = `https://via.placeholder.com/80x80/6B7280/FFFFFF?text=${member.name.split(' ').map(n => n[0]).join('')}`;
                    }}
                  />
                </div>
                <h3 class="text-base font-semibold mb-2 text-white">{member.name}</h3>
                <p class="text-yellow-400 font-medium mb-2 text-sm">{member.role}</p>
                <p class="text-gray-400 text-xs mb-1">{member.school}</p>
                <p class="text-gray-500 text-xs">{member.grade}</p>
              </div>
            {/each}
          </div>
        </div>
      </div>
    {:else if activeTab === 'missing'}
      <div class="team-content">
        <div class="mb-12">
          <div class="w-full h-80 bg-gradient-to-br from-blue-900 to-purple-900 rounded-2xl flex items-center justify-center border border-gray-700">
            <div class="text-center">
              <div class="w-24 h-24 bg-blue-500 rounded-full mx-auto mb-4 flex items-center justify-center">
                <svg class="w-12 h-12 text-white" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3z"></path>
                </svg>
              </div>
              <p class="text-gray-400">Team Photo Coming Soon</p>
            </div>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
            <h3 class="text-xl font-bold mb-4 text-blue-400">Team Information</h3>
            <div class="space-y-3">
              <div><span class="text-gray-400">Team Number:</span> <span class="text-white font-semibold">#8547</span></div>
              <div><span class="text-gray-400">Members:</span> <span class="text-white font-semibold">{missingAmpsMembers.length} Students</span></div>
              <div><span class="text-gray-400">Coach:</span> <span class="text-white font-semibold">Ms. Rodriguez</span></div>
              <div><span class="text-gray-400">Founded:</span> <span class="text-white font-semibold">2021</span></div>
              <div><span class="text-gray-400">Competition:</span> <span class="text-white font-semibold">FTC</span></div>
            </div>
          </div>
          
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
            <h3 class="text-xl font-bold mb-4 text-blue-400">Our Story</h3>
            <p class="text-gray-300 leading-relaxed">
              Missing Amps emerged from the desire to electrify the world of competitive robotics. 
              We focus on precision engineering and innovative electrical solutions. Our name reflects 
              our mission: to find the missing piece that powers extraordinary robotic performance 
              and brings energy to every challenge we face.
            </p>
          </div>
        </div>

        <div>
          <h3 class="text-2xl font-bold mb-8 text-center text-blue-400">Team Members</h3>
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
            {#each missingAmpsMembers as member}
              <div class="team-card bg-gray-900 rounded-xl border border-gray-700 p-6 text-center hover:border-gray-600 transition-all duration-300">
                <div class="w-20 h-20 mx-auto mb-4 rounded-full overflow-hidden bg-gray-700">
                  <img 
                    src={member.image} 
                    alt={member.name} 
                    class="w-full h-full object-cover"
                    on:error={(e) => {
                      e.target.src = `https://via.placeholder.com/80x80/3B82F6/FFFFFF?text=${member.name.split(' ').map(n => n[0]).join('')}`;
                    }}
                  />
                </div>
                <h3 class="text-base font-semibold mb-2 text-white">{member.name}</h3>
                <p class="text-blue-400 font-medium mb-2 text-sm">{member.role}</p>
                <p class="text-gray-400 text-xs mb-1">{member.school}</p>
                <p class="text-gray-500 text-xs">{member.grade}</p>
              </div>
            {/each}
          </div>
        </div>
      </div>
    {/if}
    </div>
  </div>
</main>
