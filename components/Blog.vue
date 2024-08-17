<template>
  <section class="blog-section py-16 px-4">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-5xl font-bold text-center mb-12 title-styling">Новости и обновления</h2>

      <!-- Список статей -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
        <div v-for="(post, index) in posts" :key="index" class="post-item bg-dark p-8 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105">
          <img v-if="post.image" :src="post.image" :alt="post.title" class="mb-6 w-full h-48 object-cover rounded-lg shadow-md border-red">
          <h3 class="text-2xl font-extrabold text-white mb-4">{{ post.title }}</h3>
          <p class="text-gray-300 mb-6">{{ post.excerpt }}</p>
          <router-link :to="post.link" class="text-pink-600 font-semibold hover:underline">Читать далее</router-link>
        </div>
      </div>

      <!-- Бэкстейдж контент -->
      <div class="backstage-content mt-20">
        <h3 class="text-4xl font-extrabold text-center mb-8 backstage-title">Эксклюзивный бэкстейдж контент</h3>
        <div class="video-container mb-12">
          <iframe
            width="100%"
            height="400"
            src="https://www.youtube.com/embed/BACKSTAGE_VIDEO_ID"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10">
          <div v-for="(image, index) in backstageImages" :key="index" class="backstage-item hover:rotate-2 transition-transform duration-300">
            <img :src="image.src" :alt="image.alt" class="w-full h-auto object-cover rounded-lg shadow-lg">
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'BlogSection',
  data() {
    return {
      posts: [
        {
          title: 'Запуск кампании на Hooandja!',
          excerpt: 'Мы рады объявить о запуске нашей кампании по сбору средств на новый клип в стиле британского рока...',
          image: 'https://example.com/blog-image1.jpg',
          link: '/blog/launch-post'
        },
        {
          title: 'Начало съемок клипа',
          excerpt: 'Съемочный процесс начался, и команда работает над воплощением нашей идеи в жизнь. Узнайте больше о первых днях...',
          image: 'https://example.com/blog-image2.jpg',
          link: '/blog/filming-start'
        },
        {
          title: 'Закулисные моменты',
          excerpt: 'В этом посте мы делимся эксклюзивными закулисными фотографиями со съемок нового клипа. Посмотрите, как это было...',
          image: 'https://example.com/blog-image3.jpg',
          link: '/blog/backstage'
        }
      ],
      backstageImages: [
        { src: 'https://example.com/backstage1.jpg', alt: 'Съемки клипа за кулисами' },
        { src: 'https://example.com/backstage2.jpg', alt: 'Группа на съемочной площадке' },
        { src: 'https://example.com/backstage3.jpg', alt: 'Режиссер и команда в работе' }
      ]
    };
  }
};
</script>

<style scoped>
.blog-section {
  background-color: #1a1a1a;
  padding-bottom: 4rem;
}

.title-styling {
  font-family: 'Courier New', monospace;
  color: #ff0054;
  text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.5);
  letter-spacing: 0.1em;
  transform: rotate(-1.5deg);
}

.post-item {
  background-color: #292929;
  border-left: 5px solid #ff0054;
}

.post-item img {
  border: 2px solid #ff0054;
}

.backstage-content {
  margin-top: 4rem;
}

.backstage-title {
  color: #ff0054;
  text-transform: uppercase;
}

.video-container iframe {
  border: 3px solid #ff0054;
}

.backstage-item img {
  transition: transform 0.3s ease-in-out;
}

.backstage-item img:hover {
  transform: rotate(3deg) scale(1.05);
}

h2, h3 {
  color: #ff0054;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
</style>
