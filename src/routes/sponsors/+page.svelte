<script>
const sponsors = [
  { 
    name: 'TechCorp', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Gold', 
    link: 'https://www.techcorp.com' 
  },
  { 
    name: 'InnovateTech', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Gold', 
    link: 'https://www.innovatetech.com' 
  },
  { 
    name: 'FutureSoft', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Gold', 
    link: 'https://www.futuresoft.com' 
  },
  
  { 
    name: 'DataDynamics', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Silver', 
    link: 'https://www.datadynamics.com' 
  },
  { 
    name: 'CloudEdge', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Silver', 
    link: 'https://www.cloudedge.com' 
  },
  { 
    name: 'VisionaryTech', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Silver', 
    link: 'https://www.visionarytech.com' 
  },
  
  { 
    name: 'CloudNine', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Bronze', 
    link: 'https://www.cloudnine.com' 
  },
  { 
    name: 'SecureNet', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Bronze', 
    link: 'https://www.securenet.com' 
  },
  { 
    name: 'SmartConnect', 
    logo: '/placeholder.svg?height=150&width=150', 
    tier: 'Bronze', 
    link: 'https://www.smartconnect.com' 
  }
];


  const tiers = ['Gold', 'Silver', 'Bronze'];
</script>

<svelte:head>
  <title>TechConf 2025 - Sponsors</title>
</svelte:head>

<main class="max-w-6xl mx-auto p-5">
  <h1 class="text-center text-3xl font-bold my-5">Our Sponsors</h1>
  {#each tiers as tier}
    <h2 class="mt-8 text-2xl font-semibold ">{tier} Sponsors</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 mt-4">
      {#each sponsors.filter(sponsor => sponsor.tier === tier) as sponsor}
        <div class="bg-[#F7F7F7] shadow-md rounded-lg p-5 border border-gray-200 flex flex-col items-center">
          <img src={"https://www.pngitem.com/pimgs/m/195-1951323_your-logo-here-png-company-logo-your-logo.png"} class="w-full object-contain" alt={sponsor.name}>
          <div class="mt-4 text-center">
            <h5 class="text-lg font-semibold">{sponsor.name}</h5>
            <a href='{sponsor.link}' class="mt-2 inline-block px-4 py-2 bg-blue-500 text-white rounded-full hover:bg-blue-600 transition-colors">Visit Website</a>
          </div>
        </div>
      {/each}
    </div>
  {/each}
</main>

<style>

</style>
