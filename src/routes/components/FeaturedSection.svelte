<script>
  const speakers = [
  {
    name: "Dr. Ramesh Kumar",
    title: "Chief Technology Officer",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Dr._Ramesh_Kumar.jpg/400px-Dr._Ramesh_Kumar.jpg",
    bio: "Dr. Ramesh Kumar is an experienced CTO with over 20 years in the technology industry, specializing in AI and Cloud computing."
  },
  {
    name: "Ms. Priya Mehta",
    title: "Senior Cloud Architect",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/a/a1/Priya_Mehta.jpg/400px-Priya_Mehta.jpg",
    bio: "Ms. Priya Mehta is a Senior Cloud Architect with expertise in cloud infrastructure, DevOps, and digital transformation in global enterprises."
  },
  {
    name: "Mr. Arvind Sharma",
    title: "Blockchain Specialist",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Arvind_Sharma.jpg/400px-Arvind_Sharma.jpg",
    bio: "Mr. Arvind Sharma is a Blockchain Specialist who has worked with multiple startups and enterprises, integrating blockchain solutions into business processes."
  },
  {
    name: "Ms. Ananya Gupta",
    title: "AI & ML Expert",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Ananya_Gupta.jpg/400px-Ananya_Gupta.jpg",
    bio: "Ms. Ananya Gupta is a leading AI & ML expert with a passion for creating intelligent systems that solve real-world problems using advanced algorithms."
  },
  {
    name: "Mr. Vikram Singh",
    title: "Cloud Solutions Architect",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/Vikram_Singh.jpg/400px-Vikram_Singh.jpg",
    bio: "Mr. Vikram Singh is a Cloud Solutions Architect with over 15 years of experience in designing scalable cloud architectures for large enterprises."
  },
  {
    name: "Dr. Sunita Patel",
    title: "Cybersecurity Expert",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Sunita_Patel.jpg/400px-Sunita_Patel.jpg",
    bio: "Dr. Sunita Patel is a renowned Cybersecurity Expert focused on creating secure, resilient networks and systems for enterprises in various sectors."
  }
];
</script>

<section id="speakers" class="py-20 bg-neutral-100">
    <div class="container mx-auto px-6 lg:px-20">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold mb-4 animate__animated animate__fadeInUp">Keynote Speakers</h2>
        <p class="text-gray-600 max-w-2xl mx-auto animate__animated animate__fadeInUp animate__delay-1s">
          Learn from industry leaders and innovators who are shaping the future of technology
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

      {#each speakers.slice(0,3) as speaker}
        <div class="bg-white rounded-xl shadow-lg overflow-hidden transform hover:scale-105 transition-all duration-300 animate__animated animate__fadeInUp">
          <div class="aspect-w-1 aspect-h-1 bg-neutral-200">
            <div class="w-full h-full flex items-center justify-center">
              <img src="/speaker1.jpg" alt="">
            </div>
          </div>
          <div class="p-6">
            <h3 class="text-xl font-bold mb-2">{speaker.name}</h3>
            <p class="text-blue-500 mb-3">{speaker.title}</p>
            <p class="text-gray-600">{speaker.bio}</p>
          </div>
        </div>

        {/each}

      </div>
       

      <div class="text-center mt-12">
        <a href="/speakers" class="bg-blue-500 hover:bg-blue-600 text-white px-8 py-3 rounded-full text-lg font-semibold transition-all duration-300">View All Speakers</a>
   
      </div>
    </div>
  </section>