<template>
  <section class="sponsor-benefits py-16 px-4 bg-gray-900">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-5xl font-bold text-center mb-12 uppercase text-white tracking-widest">Преимущества для спонсоров</h2>

      <!-- Раздел с карточками товаров -->
      <div class="rewards grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Карточка 1 -->
        <div class="reward-card relative p-8 bg-black text-white rounded-lg shadow-lg hover:shadow-2xl">
          <img src="/path/to/image1.jpg" alt="Эксклюзивный доступ" class="reward-image absolute top-0 left-0 w-full h-full object-cover opacity-40 hover:opacity-100 transition-opacity duration-500"/>
          <div class="content z-10 relative">
            <h3 class="text-2xl font-semibold mb-4">Эксклюзивный доступ</h3>
            <p class="text-lg leading-relaxed">Получите доступ к новому клипу до официального релиза.</p>
          </div>
        </div>

        <!-- Карточка 2 -->
        <div class="reward-card relative p-8 bg-black text-white rounded-lg shadow-lg hover:shadow-2xl">
          <img src="/path/to/image2.jpg" alt="Уникальные сувениры" class="reward-image absolute top-0 left-0 w-full h-full object-cover opacity-40 hover:opacity-100 transition-opacity duration-500"/>
          <div class="content z-10 relative">
            <h3 class="text-2xl font-semibold mb-4">Уникальные сувениры</h3>
            <p class="text-lg leading-relaxed">Получите эксклюзивные футболки и постеры с логотипом артиста.</p>
          </div>
        </div>

        <!-- Карточка 3 -->
        <div class="reward-card relative p-8 bg-black text-white rounded-lg shadow-lg hover:shadow-2xl">
          <img src="/path/to/image3.jpg" alt="Подписанный CD" class="reward-image absolute top-0 left-0 w-full h-full object-cover opacity-40 hover:opacity-100 transition-opacity duration-500"/>
          <div class="content z-10 relative">
            <h3 class="text-2xl font-semibold mb-4">Подписанный CD</h3>
            <p class="text-lg leading-relaxed">Получите подписанный CD с новым альбомом и личное письмо от артиста.</p>
          </div>
        </div>

        <!-- Карточка 4 -->
        <div class="reward-card relative p-8 bg-black text-white rounded-lg shadow-lg hover:shadow-2xl">
          <img src="/path/to/image4.jpg" alt="Бэкстейдж-видео" class="reward-image absolute top-0 left-0 w-full h-full object-cover opacity-40 hover:opacity-100 transition-opacity duration-500"/>
          <div class="content z-10 relative">
            <h3 class="text-2xl font-semibold mb-4">Бэкстейдж-видео</h3>
            <p class="text-lg leading-relaxed">Доступ к закулисным съемкам клипа и эксклюзивным материалам.</p>
          </div>
        </div>

        <!-- Карточка 4 -->
        <div class="reward-card relative p-8 bg-black text-white rounded-lg shadow-lg hover:shadow-2xl">
          <img src="/path/to/image4.jpg" alt="Бэкстейдж-видео" class="reward-image absolute top-0 left-0 w-full h-full object-cover opacity-40 hover:opacity-100 transition-opacity duration-500"/>
          <div class="content z-10 relative">
            <h3 class="text-2xl font-semibold mb-4">Cпонсор</h3>
            <p class="text-lg leading-relaxed">Упоминание в титрах клипа как официального спонсора.</p>
          </div>
        </div>

        <!-- Карточка 4 -->
        <div class="reward-card relative p-8 bg-black text-white rounded-lg shadow-lg hover:shadow-2xl">
          <img src="/path/to/image4.jpg" alt="Бэкстейдж-видео" class="reward-image absolute top-0 left-0 w-full h-full object-cover opacity-40 hover:opacity-100 transition-opacity duration-500"/>
          <div class="content z-10 relative">
            <h3 class="text-2xl font-semibold mb-4">Эксклюзивная встреча</h3>
            <p class="text-lg leading-relaxed">Эксклюзивная встреча с артистом для обсуждения его творчества и планов.</p>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
  
  <script>
  export default {
    name: 'SponsorBenefits',
    data() {
      return {
        // Здесь можно добавить динамические данные, если потребуется
      };
    },
  };
  </script>
  
  <style scoped>
  .sponsor-benefits {
  background-color: #111; /* Темный фон для раздела */
  color: #fff;
}

.sponsor-benefits h2 {
  color: #ff0054; /* Акцентный цвет заголовка */
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-bottom: 3rem;
}

.reward-card {
  position: relative;
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border: 3px solid transparent;
  background-color: #1a1a1a;
}

.reward-card:hover {
  transform: rotate(-2deg) scale(1.05);
  box-shadow: 0 8px 20px rgba(255, 255, 255, 0.2);
  border-color: #ff0054;
}

.reward-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0.4;
  z-index: 1;
  transition: opacity 0.5s;
}

.reward-card:hover .reward-image {
  opacity: 1;
}

.content {
  position: relative;
  z-index: 10;
}

.reward-card h3 {
  font-size: 1.75rem;
  margin-bottom: 1rem;
  color: #ff0054;
  text-transform: uppercase;
}

.reward-card p {
  font-size: 1.2rem;
  line-height: 1.6;
  color: #f1f1f1;
}

  </style>