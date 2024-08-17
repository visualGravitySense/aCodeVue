<template>
  <section class="support-section py-16 px-4">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-5xl font-extrabold text-center mb-12 title-styling">Как поддержать проект</h2>

      <!-- Описание шагов поддержки -->
      <div class="steps-to-support mb-12">
        <h3 class="text-3xl font-bold mb-6 steps-title">Шаги для поддержки проекта на Hooandja</h3>
        <ol class="list-decimal list-inside text-xl text-gray-800">
          <li>Зарегистрируйтесь на платформе <a href="https://www.hooandja.ee" target="_blank" class="text-orange-500 hover:underline">Hooandja</a>.</li>
          <li>Найдите наш проект, введя его название в строку поиска.</li>
          <li>Выберите сумму поддержки, которую хотите внести, и выберите соответствующее вознаграждение.</li>
          <li>Подтвердите платеж, следуя инструкциям на сайте.</li>
          <li>После подтверждения, ждите получения вознаграждения, как указано в описании кампании.</li>
        </ol>
      </div>

      <!-- Интеграция социальных сетей -->
      <div class="social-share text-center">
        <h3 class="text-3xl font-bold mb-6 social-title">Поделитесь этим проектом в социальных сетях</h3>
        <div class="social-buttons flex justify-center gap-6">
          <a href="https://www.facebook.com/sharer/sharer.php?u=https://hooandja.ee/project-link" target="_blank" class="social-btn bg-blue-700 text-white px-6 py-3 rounded-full shadow-lg hover:scale-105 transition-transform">
            Facebook
          </a>
          <a href="https://twitter.com/intent/tweet?url=https://hooandja.ee/project-link" target="_blank" class="social-btn bg-blue-500 text-white px-6 py-3 rounded-full shadow-lg hover:scale-105 transition-transform">
            Twitter
          </a>
          <a href="https://www.linkedin.com/shareArticle?mini=true&url=https://hooandja.ee/project-link" target="_blank" class="social-btn bg-blue-800 text-white px-6 py-3 rounded-full shadow-lg hover:scale-105 transition-transform">
            LinkedIn
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SupportSection',
};
</script>

<style scoped>
.support-section {
  background-color: #1a1a1a;
  padding-bottom: 4rem;
}

.title-styling {
  font-family: 'Comic Sans MS', cursive, sans-serif;
  color: #ff6f61;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
  transform: rotate(-2deg);
}

.steps-title {
  color: #ff6f61;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  font-family: 'Courier New', monospace;
}

.social-title {
  color: #ff6f61;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  font-family: 'Courier New', monospace;
}

ol.list-decimal li {
  margin-bottom: 1rem;
  font-family: 'Arial', sans-serif;
}

.social-buttons .social-btn {
  transition: transform 0.3s ease-in-out, background-color 0.3s ease-in-out;
}

.social-btn:hover {
  transform: scale(1.1) rotate(-2deg);
  background-color: #ff6f61;
}
</style>