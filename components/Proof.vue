<template>
  <section class="social-proof py-16 px-4">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-6xl font-bold text-center uppercase tracking-widest mb-12 neon-text">Социальные доказательства</h2>

      <!-- Отзывы и поддержка -->
      <div class="reviews grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
        <div
          v-for="(review, index) in reviews"
          :key="index"
          class="review-card relative p-8 rounded-lg shadow-xl transform hover:rotate-1 hover:scale-105 transition duration-500"
        >
          <p class="text-xl italic leading-snug">"{{ review.text }}"</p>
          <p class="text-right mt-4 font-bold text-2xl uppercase neon-text">- {{ review.author }}</p>
          <div class="absolute top-0 right-0 p-2 bg-pink-500 text-white text-sm uppercase font-bold rounded-bl-lg">New</div>
        </div>
      </div>

      <!-- Счетчик прогресса -->
      <div class="progress-tracker text-center mb-12">
        <h3 class="text-4xl font-bold uppercase mb-8 neon-text">Прогресс кампании</h3>
        <div class="progress-bar-container w-full bg-gray-800 rounded-full h-6 relative mb-4">
          <div class="progress-bar bg-gradient-to-r from-pink-600 to-yellow-500 h-6 rounded-full" :style="{ width: progressPercentage + '%' }"></div>
          <div class="absolute left-0 top-0 h-6 bg-black w-full opacity-50 skew-x-12"></div>
        </div>
        <p class="text-3xl text-white">{{ progressPercentage }}% собрано!</p>
      </div>

      <!-- Кнопка для перехода на страницу кампании -->
      <div class="text-center">
        <a href="https://hooandja.com/project" target="_blank" class="neon-button inline-block px-8 py-3 rounded-full text-lg font-bold uppercase">
          Посмотреть кампанию
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SocialProof',
  data() {
    return {
      reviews: [
        {
          text: 'Это невероятный проект! Я уверен, что клип станет настоящим шедевром.',
          author: 'Джон Смит, музыкальный продюсер'
        },
        {
          text: 'Поддерживаю этот проект, потому что это важная веха в музыкальной карьере артиста.',
          author: 'Анна Иванова, поклонница'
        },
        {
          text: 'Этот клип будет настоящим открытием для фанатов рока!',
          author: 'Майкл Джонсон, музыкальный критик'
        },
        {
          text: 'Такого проекта музыкальная индустрия ещё не видела. Это что-то совершенно новое.',
          author: 'Сара Уилсон, режиссер'
        }
      ],
      progressPercentage: 75
    };
  }
};
</script>

<style scoped>
.social-proof {
  background-color: #000; /* Глубокий черный фон */
  color: #fff;
  position: relative;
  overflow: hidden;
}

.neon-text {
  color: #ff0054; /* Яркий розовый акцент */
  text-shadow: 0 0 10px rgba(255, 0, 84, 0.7), 0 0 20px rgba(255, 0, 84, 0.6);
}

.review-card {
  background-color: #111; /* Темный цвет карточки */
  border-left: 5px solid #ff0054;
}

.review-card:hover {
  border-left-color: #ffff00; /* Меняем цвет при наведении */
}

.progress-bar-container {
  position: relative;
  height: 6px;
}

.progress-bar {
  transition: width 0.4s ease;
}

.neon-button {
  background: linear-gradient(135deg, #ff0054, #ffff00);
  color: #000;
  box-shadow: 0 0 15px rgba(255, 0, 84, 0.6);
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
}

.neon-button:hover {
  box-shadow: 0 0 25px rgba(255, 0, 84, 1), 0 0 35px rgba(255, 255, 0, 0.8);
  transform: scale(1.05);
}
</style>