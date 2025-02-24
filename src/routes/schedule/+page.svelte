<script>
  const schedule = [
    { date: '2025-03-15', time: '09:00 AM', topic: 'Opening Keynote', speaker: 'John Doe' },
    { date: '2025-03-15', time: '10:30 AM', topic: 'The Future of Blockchain', speaker: 'Jane Smith' },
    { date: '2025-03-15', time: '01:00 PM', topic: 'Quantum Computing: A New Era', speaker: 'Alex Johnson' },
    { date: '2025-03-16', time: '09:00 AM', topic: 'Cybersecurity in the Age of AI', speaker: 'Emily Brown' },
    { date: '2025-03-16', time: '10:30 AM', topic: 'VR/AR: Reshaping Human Interaction', speaker: 'Michael Lee' },
    { date: '2025-03-16', time: '01:00 PM', topic: 'IoT: Connecting the World', speaker: 'Sarah Davis' }
  ];

  let filteredSchedule = schedule;
  let activeFilter = 'all';

  function filterByDay(day) {
    filteredSchedule = schedule.filter(session => session.date === day);
    activeFilter = day;
  }

  function resetFilter() {
    filteredSchedule = schedule;
    activeFilter = 'all';
  }
</script>

<svelte:head>
  <title>TechConf 2025 - Schedule</title>
</svelte:head>

<section id="schedule" class="py-20 bg-white">
  <div class="container mx-auto px-6">
    <div class="text-center mb-16">
      <h2 class="text-4xl font-bold mb-4">Conference Schedule</h2>
      <p class="text-gray-600 max-w-2xl mx-auto mb-8">
        Two days packed with inspiring talks, workshops, and networking opportunities
      </p>

      <div class="flex justify-center space-x-4 mb-12">
        <button class="px-6 py-2 rounded-full  hover:bg-blue-500 hover:text-white transition-colors  {activeFilter === 'all' ? 'bg-blue-500 text-white' : 'bg-neutral-200'}" on:click={resetFilter}>All Days</button>
        <button class="px-6 py-2 rounded-full  hover:bg-blue-500 hover:text-white transition-colors {activeFilter === '2025-03-15' ? 'bg-blue-500 text-white' : 'bg-neutral-200'}"  on:click={() => filterByDay('2025-03-15')}>Day 1</button>
        <button class="px-6 py-2 rounded-full hover:bg-blue-500 hover:text-white transition-colors {activeFilter === '2025-03-16' ? 'bg-blue-500 text-white' : 'bg-neutral-200'}" on:click={() => filterByDay('2025-03-16')}>Day 2</button>
      </div>
    </div>

    <div class="space-y-6">
      {#each filteredSchedule as session}
        <div class="bg-neutral-50 rounded-xl p-6 shadow-md">
          <div class="flex flex-col md:flex-row md:items-center justify-between">
            <div class="mb-4 md:mb-0">
              <span class="text-blue-500 font-semibold me-5"><i class="fa-solid fa-calendar-days me-2"></i>{session.date}</span>
              <span class="text-blue-500 font-semibold"><i class="fa-solid fa-clock me-2"></i>{session.time}</span>
              <h3 class="text-xl font-bold mt-2">{session.topic}</h3>
              <p class="text-gray-600">{session.speaker} - {session.track}</p>
            </div>
            <button class="bg-blue-500 text-white px-4 py-2 rounded-full hover:bg-blue-600 transition-colors">
              Add to Calendar
            </button>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
