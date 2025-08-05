<script>
  import IconLogo from "../../lib/images/logo.png";
  import akshat from "../../lib/family/akshat_kumar.png";
  import punit from "../../lib/family/punit_lakhotiya.png";
  import navin from "../../lib/family/navin_rao.png";
  import lucas from "../../lib/family/lucas_silva.png";
  import swaraj from "../../lib/family/swaraj_nibandhe.png";
  import xander from "../../lib/family/xander_kuksov.png";
  import samanyu from "../../lib/family/samanyu_earna.png";
  import azalea from "../../lib/family/azalea_tang.png";
  import ainesh from "../../lib/family/ainesh_gupta.png";
  import erik from "../../lib/family/erik_wang.png";
  import mahit from "../../lib/family/mahit_cherku.png";
  import vedant from "../../lib/family/vedant_teware.png";
  import ashwin from "../../lib/family/ashwin_gupta.png";
  import rishabh from "../../lib/family/rishabh_singh.png";
  import nishant from "../../lib/family/nishant_sinari.png";
  import team from "../../lib/family/teamphoto.png";


  
  let activeTab = 'undefined';

  const undefinedTeamMembers = [
    {
      name: "Akshat Kumar",
      grade: "12th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano Senior High School",
      image: akshat
    },
    {
      name: "Neel M",
      grade: "11th Grade",
      role: "Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/44BsdgkP/Neel-PFP.webp"
    },
    {
      name: "Rishabh Singh",
      grade: "12th Grade",
      role: "Chief Technical Officer",
      school: "Plano West Senior High School",
      image: rishabh
    },
    {
      name: "Punit Lakhotiya",
      grade: "12th Grade",
      role: "Finance/Team Management/Engineer",
      school: "Plano West Senior High School",
      image: punit
    },

    {
      name: "Navin Rao",
      grade: "12th Grade",
      role: "CAD Modeler/Engineer",
      school: "Plano Senior High School",
      image: navin
    },
    {
      name: "Lucas Silva",
      grade: "12th Grade",
      role: "Engineer/Driver",
      school: "Plano West Senior High School",
      image: lucas
    },
    {
      name: "Swaraj Nibandhe",
      grade: "12th Grade",
      role: "Engineer/Team Lead",
      school: "Plano West Senior High School",
      image: swaraj
    },
    {
      name: "Xander Kuksov",
      grade: "12th Grade",
      role: "Programmer",
      school: "Plano West Senior High School",
      image: xander
    },
    {
      name: "Samanyu Earna",
      grade: "12th Grade",
      role: "Programmer",
      school: "Plano West Senior High School",
      image: samanyu
    },
    {
      name: "Azalea Tang",
      grade: "12th Grade",
      role: "Programmer",
      school: "Plano West Senior High School",
      image: azalea
    },
    {
      name: "Ainesh Gupta",
      grade: "12th Grade",
      role: "Engineer",
      school: "Plano West Senior High School",
      image: ainesh
    },
    {
      name: "Erik Wang",
      grade: "12th Grade",
      role: "Engineer/Outreach/Driver",
      school: "Plano West Senior High School",
      image: erik
    },
    {
      name: "Mahit Cherku",
      grade: "12th Grade",
      role: "Outreach/Engineer",
      school: "Memorial High School",
      image: mahit
    },
    {
      name: "Vedant Teware",
      grade: "12th Grade",
      role: "Outreach/Engineer",
      school: "Lonestar High School",
      image: vedant
    },
    {
      name: "Ashwin Gupta",
      grade: "12th Grade",
      role: "Engineer",
      school: "Plano Senior High School",
      image: ashwin
    },
    {
      name: "Nishant Sinari",
      grade: "12th Grade",
      role: "Outreach/CAD Lead",
      school: "Plano West Senior High School",
      image: nishant
    },
    
  ];

  // Dummy data for Missing Amps team
  const missingAmpsMembers = [
    {
      name: "Neel T.",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/44BsdgkP/Neel-PFP.webp"
    },
    {
      name: "Harsheel Desai",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://images.emojiterra.com/twitter/v14.0/1024px/1f633.png"
    },
    {
      name: "Ishaan N.",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/7L0qYJwJ/Ishaan-PFP.webp"
    },
    {
      name: "Aarav B.",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/SxbTbnTv/AlooPFP.webp"
    },
    {
      name: "Rishabh M.",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/FRFFWsXf/Rishabh-Zest.webp"
    },
    {
      name: "Goutham R.",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/VNJPdrwW/Goutham-Goon.webp"
    },
    {
      name: "Hrudhai L.",
      grade: "11th Grade",
      role: "Captain/CAD Modeler/Engineer",
      school: "Plano West Senior High School",
      image: "https://i.postimg.cc/52r0VSg9/cropped-image-min.png"
    },
    
  ];

  // Chiefs (specified names)
  const chiefNames = ["Akshat Kumar", "Rishabh Singh", "Punit Lakhotiya", "Neel M", "Swaraj Nibandhe"];
  // Map leadership roles and names for display only
  const chiefs = [
    {
      ...undefinedTeamMembers.find(m => m.name === "Akshat Kumar"),
      role: "Founder & President",
      grade: "12th Grade"
    },
    {
      ...undefinedTeamMembers.find(m => m.name === "Rishabh Singh"),
      role: "Chief Technical Officer",
      grade: "12th Grade"
    },
    {
      ...undefinedTeamMembers.find(m => m.name === "Punit Lakhotiya"),
      role: "Chief Financial Officer",
      grade: "12th Grade"
    },
    {
      ...undefinedTeamMembers.find(m => m.name === "Swaraj Nibandhe"),
      role: "Chief Operating Officer",
      grade: "12th Grade"
    },
    {
      ...undefinedTeamMembers.find(m => m.name === "Neel M"),
      name: "Neel Tipnis",
      role: "Head of Expansions",
      grade: "11th Grade"
    }
  ];

  // All team members (including chiefs)
  // No filtering, so chiefs will appear in both sections




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
            Undefined
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
          <div class="w-full h-96 rounded-2xl overflow-hidden border border-gray-700">
            <img src={team} alt="Undefined Robotics Team" class="w-full h-full object-cover"/>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700 md:col-span-1">
            <h3 class="text-xl font-bold mb-4 text-yellow-400">Team Information</h3>
            <div class="space-y-3">
              <div><span class="text-gray-400">Team Number:</span> <span class="text-white font-semibold">#25782</span></div>
              <div><span class="text-gray-400">Members:</span> <span class="text-white font-semibold">{undefinedTeamMembers.length-4} Seniors</span></div>
              <div><span class="text-gray-400">Founded:</span> <span class="text-white font-semibold">2024</span></div>
              <div><span class="text-gray-400">Competition:</span> <span class="text-white font-semibold">FTC FiT S-League</span></div>
            </div>
          </div>
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700 md:col-span-2">
            <h3 class="text-xl font-bold mb-4 text-yellow-400">Our Story</h3>
            <p class="text-gray-300 leading-relaxed">
              Undefined was born from a shared passion for innovation and problem-solving. 
              Our team combines diverse talents in engineering, programming, and design to create 
              cutting-edge robotic solutions. We believe in pushing boundaries and exploring the 
              undefined possibilities of robotics technology.
            </p>
          </div>
        </div>

        <div>
          <h3 class="text-2xl font-bold mb-8 text-center text-yellow-400">Team Members</h3>
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
            {#each undefinedTeamMembers.filter(member => member.name !== 'Rishabh Singh' && member.name !== 'Neel M') as member}
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

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">

          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700 md:col-span-1">
            <h3 class="text-xl font-bold mb-4 text-blue-400"><a href="https://www.missingamps.team/" target="_blank" rel="noopener noreferrer">Team Information</a></h3>
            <div class="space-y-3">
              <div><span class="text-gray-400">Team Number:</span> <span class="text-white font-semibold">#30801</span></div>
              <div><span class="text-gray-400">Members:</span> <span class="text-white font-semibold">{missingAmpsMembers.length} Juniors</span></div>
              <div><span class="text-gray-400">Founded:</span> <span class="text-white font-semibold">2025</span></div>
              <div><span class="text-gray-400">Competition:</span> <span class="text-white font-semibold">FTC FiT F-League</span></div>
            </div>
          </div>
          <div class="bg-gray-900 p-6 rounded-xl border border-gray-700 md:col-span-2">
            <h3 class="text-xl font-bold mb-4 text-blue-400"><a href="https://www.missingamps.team/" target="_blank" rel="noopener noreferrer">Our Story</a></h3>
            <p class="text-gray-300 leading-relaxed">
              <a href="https://www.missingamps.team/" target="_blank" rel="noopener noreferrer">Missing Amps</a> is a passionate robotics team founded by alumni of Jasper High School’s award-winning FTC team (#11419).
              With experience at the UIL State Championship, we now compete in the FIRST® Tech Challenge while giving back through STEM outreach.
              Our mission is to inspire the next generation of innovators by engaging local youth, partnering with businesses, and building a strong platform for future STEM leaders.
            </p>
          </div>
        </div>

        <div>
          <h3 class="text-2xl font-bold mb-8 text-center text-blue-400"><a href="https://www.missingamps.team/" target="_blank" rel="noopener noreferrer">Team Members</a></h3>
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
