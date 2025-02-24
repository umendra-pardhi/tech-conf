<script>
    import Header from './Header.svelte';
    import { onMount } from 'svelte';
    // import  '../static/index.svg';
  
    let days = '00';
    let hours = '00';
    let minutes = '00';
    let seconds = '00';
  
    // Countdown Timer
    const updateCountdown = () => {
      const eventDate = new Date('February 26, 2025 00:00:00').getTime();
      const now = new Date().getTime();
      const distance = eventDate - now;
  
      days = String(Math.floor(distance / (1000 * 60 * 60 * 24))).padStart(2, '0');
      hours = String(Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))).padStart(2, '0');
      minutes = String(Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))).padStart(2, '0');
      seconds = String(Math.floor((distance % (1000 * 60)) / 1000)).padStart(2, '0');
    };
  
    onMount(() => {
      setInterval(updateCountdown, 1000);
      updateCountdown(); // Initialize on mount
    });
  </script>
  

  <section id="hero" class="bg-neutral-900  text-white pt-42 sm:pt-38 pb-16 min-h-[100vh] sm:min-h-[80vh]  relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 z-0">
      <div class="absolute inset-0 bg-[url('/index.svg')] bg-no-repeat bg-center bg-cover"></div>
      <div class="absolute h-full w-full bg-[radial-gradient(circle_500px_at_50%_200px,rgba(96,165,250,0.1),transparent)]"></div>
    </div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center max-w-4xl mx-auto">
        <h1 class="text-4xl md:text-6xl font-bold mb-6 animate__animated animate__fadeInDown">
          TechConf 2025
        </h1>
        <p class="text-xl md:text-2xl text-gray-300 mb-8 animate__animated animate__fadeInUp animate__delay-1s">
          Join the Future of Technology: Where Innovation Meets Inspiration
        </p>
        <div class="mb-12 animate__animated animate__fadeInUp animate__delay-2s">
          <div id="countdown" class="flex justify-center gap-4 md:gap-8 mb-8">
            <div class="text-center">
              <div class="text-3xl md:text-4xl font-bold">{days}</div>
              <div class="text-sm text-gray-400">Days</div>
            </div>
            <div class="text-center">
              <div class="text-3xl md:text-4xl font-bold">{hours}</div>
              <div class="text-sm text-gray-400">Hours</div>
            </div>
            <div class="text-center">
              <div class="text-3xl md:text-4xl font-bold">{minutes}</div>
              <div class="text-sm text-gray-400">Minutes</div>
            </div>
            <div class="text-center">
              <div class="text-3xl md:text-4xl font-bold">{seconds}</div>
              <div class="text-sm text-gray-400">Seconds</div>
            </div>
          </div>
        </div>
        <div class="space-x-4 animate__animated animate__fadeInUp animate__delay-3s">
          <button class="bg-blue-500 hover:bg-blue-600 text-white px-8 py-3 rounded-full text-lg font-semibold transition-all duration-300 transform hover:scale-105">
            Register Now
          </button>
          <a href="/about" class="border border-blue-500 text-blue-500 hover:bg-blue-500 hover:text-white px-8 py-3 rounded-full text-lg font-semibold transition-all duration-300">
            Learn More
          </a>
        </div>
      </div>
    </div>
  </section>
  
  <style>
    
  </style>
  