<script>
    import IconLogo from "../../lib/images/logo.png";
  
    const teamMembers = [
  {
    name: "Akshat Kumar",
    grade: "11th Grade",
    role: "Captain/CAD Modeler/Engineer",
    school: "Plano Senior High School",
    image: "https://www.undefinedrobotics.org/akshat_kumar.png"
  },
  {
    name: "Navin Rao",
    grade: "11th Grade",
    role: "CAD Modeler/Engineer",
    school: "Plano Senior High School",
    image: "https://www.undefinedrobotics.org/navin_rao.png"
  },
  {
    name: "Punit Lakhotiya",
    grade: "11th Grade",
    role: "Finance/Team Management/Engineer",
    school: "Plano West Senior High School",
    image: "https://www.undefinedrobotics.org/punit_lakhotiya.png"
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
  </script>
  
  <style>
    .dm-sans {
      font-family: "DM Sans", sans-serif;
      font-optical-sizing: auto;
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
  
    .member-card {
      transition: all 0.3s ease;
    }
  
    .member-card:hover {
      transform: translateY(-5px);
    }
  </style>
  
  <main class="text-white mt-40 mb-20 dm-sans">
    <div class="absolute inset-0 bg-[radial-gradient(rgba(255,255,255,0.2)_1px,transparent_1px)] bg-[size:80px_80px] z-0"></div>

    <div class="absolute inset-0 z-0">
        <div class="absolute inset-0 bg-gradient-to-r from-yellow-500 to-yellow-200 rounded-full blur-3xl opacity-5 transform -translate-y-1/2 "></div>
        <div class="absolute inset-0 bg-gradient-to-r from-yellow-200 to-yellow-700 rounded-full blur-3xl opacity-5 transform translate-y-1/2"></div>
      </div>

    <!-- Team Members Grid -->
    <section class="relative z-10 px-4">
      <div class="max-w-[80%] mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-32">
          {#each teamMembers as member}
            <div class="group bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 hover:bg-white/10 hover:border-yellow-400/40 transition-all duration-300 hover:scale-105 hover:shadow-xl hover:shadow-yellow-500/10">
              <div class="flex flex-col items-center text-center space-y-4">
                <!-- Profile Image -->
                <div class="relative">
                  <div class="absolute inset-0 bg-gradient-to-r from-yellow-500 to-yellow-300 rounded-full blur opacity-30 group-hover:opacity-50 transition-opacity duration-300"></div>
                  <img 
                    src={member.image} 
                    alt={member.name} 
                    class="w-30 h-30 rounded-full object-cover border border-white/20 relative z-10 group-hover:border-yellow-400/50 transition-colors duration-300" 
                  />
                </div>
                
                <!-- Member Info -->
                <div class="space-y-2">
                  <h3 class="text-lg font-semibold text-white group-hover:text-yellow-300 transition-colors duration-300">
                    {member.name}
                  </h3>
                  <p class="text-yellow-400 text-sm font-medium">
                    {member.grade}
                  </p>
                  <p class="text-gray-300 text-sm leading-relaxed">
                    {member.role}
                  </p>
                  <p class="text-gray-400 text-xs pt-1">
                    {member.school}
                  </p>
                </div>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </section>
  </main>