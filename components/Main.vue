<template>
    <section class="bg-image text-white py-16">
      <div class="overlay"></div>
      <div class="container mx-auto flex flex-col items-center text-center px-4">
        <!-- Заголовок -->
        <h1 class="text-4xl md:text-6xl font-bold mb-6">
          Поддержите новый клип Альберта Петенберга и станьте частью музыкального приключения!
        </h1>
  
        <!-- Баннер с фото -->
        <!-- <div class="mb-8">
          <img
              src="/assets/img/preview-2.jpg"
              alt="Артист в стиле британского рока"
              class="rounded-lg shadow-lg max-w-full h-auto"
            />
          </div> -->
  
        <!-- Видеоблок -->
        <div class="mb-10 w-full md:w-2/3 lg:w-1/2">
          <iframe
            class="w-full rounded-lg shadow-lg"
            width="560" 
            height="315" 
            src="https://www.youtube.com/embed/xqAPGGthGiE" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
          </iframe>
        </div>
  
        <!-- Кнопка с призывом к действию -->
        <a
          href="https://hooandja.com/campaign-link"
          target="_blank"
          class="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-8 rounded-lg shadow-lg transition duration-300 ease-in-out"
        >
          Поддержать на Hooandja
        </a>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'HeroSection',
  }
  </script>
  
  <style scoped>
  /* Добавьте кастомные стили при необходимости */
  .bg-image {
  position: relative;
  background-image: url('@/assets/img/preview-2.jpg'); /* Укажите путь к вашему изображению */
  background-size: cover;
  background-position: center;
  height: 100%; /* Убедитесь, что секция занимает всю высоту */
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Черный цвет с 50% прозрачностью */
  z-index: 1; /* Поместите затемнение позади текста */
}

.container {
  position: relative; /* Поместите текст поверх затемненного фона */
  z-index: 2; /* Поместите текст выше затемнения */
}

  </style>