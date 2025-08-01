<script>
  import IconLogo from "../images/logo.png";
  import { faInstagram, faYoutube, faDiscord } from '@fortawesome/free-brands-svg-icons';
  import { faEnvelope } from '@fortawesome/free-solid-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';

</script>

<footer class=" backdrop-blur-sm border-t border-white/10 text-white dm-sans">

    <div class="max-w-7xl mx-auto px-4 py-12">
      <div class="grid md:grid-cols-4 gap-8">
        <div class="md:col-span-2">
          <div class="flex items-center space-x-3 mb-4">
            <img src={IconLogo} alt="Undefined Robotics Logo" class="h-12 w-12" />
            <span class="text-2xl font-bold">Undefined Robotics</span>
          </div>
          <p class="text-gray-400 max-w-md mb-6">
            A high school level private robotics team based in Plano, Texas, promoting a culture of learning and STEM in our community.
          </p>

          <div class="flex space-x-6  mt-8">
            <a
              href="https://www.instagram.com/undefinedrobotics"
              aria-label="Instagram"
              class="text-gray-400 hover:text-yellow-400 transition-colors"
              target="_blank"
              rel="noopener noreferrer"
            >
              <FontAwesomeIcon icon={faInstagram} class="w-6 h-6" />
            </a>
          
            <a
              href="https://www.youtube.com/@undefinedrobotics"
              aria-label="YouTube"
              class="text-gray-400 hover:text-yellow-400 transition-colors"
              target="_blank"
              rel="noopener noreferrer"
            >
              <FontAwesomeIcon icon={faYoutube} class="w-8 h-6" />
            </a>
          
            <p class="text-gray-400 hover:text-yellow-400 transition-colors">
              <FontAwesomeIcon icon={faDiscord} class="w-6 h-6" />
              <span>
                - undefinedrobotics
              </span>
          </p>
          </div>
                  </div>
        
        <div>
          <h3 class="text-lg font-semibold mb-4">Quick Links</h3>
          <ul class="space-y-2">
            <li><a href="/family" class="text-gray-400 hover:text-yellow-400 transition-colors">Our Family</a></li>
            <li><a href="/contact" class="text-gray-400 hover:text-yellow-400 transition-colors">Contact</a></li>
            <li><a href="/impact" class="text-gray-400 hover:text-yellow-400 transition-colors">Impact</a></li>
            <li><a href="/record" class="text-gray-400 hover:text-yellow-400 transition-colors">Record</a></li>
          </ul>
        </div>
        
        <div>
          <h3 class="text-lg font-semibold mb-4">Contact Info</h3>
          <div class="space-y-2 text-gray-400">
            <p>📍 Plano, Texas</p>
            <p>📧 team@undefinedrobotics.org</p>
            <p>📧 missingamps.ftc@gmail.com</p>
            <p>📱 (469) 819-7461</p>
          </div>
        </div>
      </div>
      
      <div class="border-t border-white/10 mt-8 pt-6 flex flex-col md:flex-row justify-between items-center">
        <p class="text-gray-400 text-sm">
          © 2025 Undefined Robotics. All rights reserved.
        </p>
        <div class="flex space-x-6 mt-4 md:mt-0">
          <a href="#" class="text-gray-400 hover:text-yellow-400 transition-colors text-sm">Privacy Policy</a>
          <a href="#" class="text-gray-400 hover:text-yellow-400 transition-colors text-sm">Terms of Service</a>
          <a href="#" class="text-gray-400 hover:text-yellow-400 transition-colors text-sm">Code of Conduct</a>
        </div>
      </div>
    </div>
  </footer>