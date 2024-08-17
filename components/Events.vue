<template>
  <section class="events-section py-16 px-4">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-5xl font-bold text-center mb-12 title-styling">Расписание и события</h2>

      <!-- Физические мероприятия -->
      <div class="physical-events mb-12">
        <h3 class="text-4xl font-semibold mb-6 subtitle-styling">Гастроли и концерты</h3>
        <ul class="list-none">
          <li v-for="(event, index) in physicalEvents" :key="index" class="mb-8">
            <div class="event-card bg-dark-gray p-6 rounded-lg shadow-lg hover:shadow-2xl transition-shadow duration-300">
              <div class="flex flex-col md:flex-row md:items-center">
                <div class="flex-1 md:mr-6">
                  <h4 class="text-2xl font-bold text-light-gray">{{ event.title }}</h4>
                  <p class="text-light-gray">{{ event.date }}</p>
                  <p class="text-gray-400">{{ event.location }}</p>
                  <p class="text-gray-300 mt-2">{{ event.description }}</p>
                </div>
                <a :href="event.link" target="_blank" class="mt-4 md:mt-0 text-pink-500 hover:text-pink-400 font-semibold">
                  Подробнее
                </a>
              </div>
            </div>
          </li>
        </ul>
      </div>

      <!-- Виртуальные мероприятия -->
      <div class="virtual-events">
        <h3 class="text-4xl font-semibold mb-6 subtitle-styling">Виртуальные встречи и стримы</h3>
        <ul class="list-none">
          <li v-for="(event, index) in virtualEvents" :key="index" class="mb-8">
            <div class="event-card bg-dark-gray p-6 rounded-lg shadow-lg hover:shadow-2xl transition-shadow duration-300">
              <div class="flex flex-col md:flex-row md:items-center">
                <div class="flex-1 md:mr-6">
                  <h4 class="text-2xl font-bold text-light-gray">{{ event.title }}</h4>
                  <p class="text-light-gray">{{ event.date }}</p>
                  <p class="text-gray-300 mt-2">{{ event.description }}</p>
                </div>
                <a :href="event.link" target="_blank" class="mt-4 md:mt-0 text-pink-500 hover:text-pink-400 font-semibold">
                  Присоединиться
                </a>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'EventsSection',
  data() {
    return {
      physicalEvents: [
        {
          title: 'Концерт в Москве',
          date: '15 сентября 2024',
          location: 'Клуб XYZ, Москва',
          description: 'Энергичный концерт с живым исполнением лучших хитов артиста.',
          link: 'https://example.com/concert-moscow'
        },
        {
          title: 'Гастроли по Европе',
          date: '01-15 октября 2024',
          location: 'Европейские города',
          description: 'Серия концертов по ключевым городам Европы.',
          link: 'https://example.com/europe-tour'
        }
      ],
      virtualEvents: [
        {
          title: 'Виртуальный стрим с артистом',
          date: '20 сентября 2024, 19:00',
          description: 'Присоединяйтесь к эксклюзивному стриму с обсуждением нового клипа и ответами на вопросы фанатов.',
          link: 'https://example.com/virtual-stream'
        },
        {
          title: 'Онлайн-встреча с фанатами',
          date: '25 сентября 2024, 17:00',
          description: 'Виртуальная встреча, где можно пообщаться с артистом и узнать больше о процессе создания клипа.',
          link: 'https://example.com/virtual-meetup'
        }
      ]
    };
  }
};
</script>

<style scoped>
.events-section {
  background-color: #121212;
  color: #e0e0e0;
  padding-bottom: 4rem;
  padding-top: 4rem;
}

.title-styling {
  font-family: 'Courier New', monospace;
  color: #ff007f;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  letter-spacing: 0.1em;
  transform: rotate(-1deg);
}

.subtitle-styling {
  color: #ff007f;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
}

.event-card {
  background-color: #1e1e1e;
}

.text-light-gray {
  color: #b0b0b0;
}

.text-gray-400 {
  color: #a0a0a0;
}

.text-gray-300 {
  color: #888;
}

.text-pink-500 {
  color: #ff007f;
}

.text-pink-500:hover {
  color: #e60073;
}

.shadow-lg {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
}

.shadow-2xl {
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.5);
}
</style>
