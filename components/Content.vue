<template>
  <section class="media-content py-16 px-4">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-5xl font-bold text-center mb-12 title-styling">Музыка и видео</h2>

      <!-- Проигрыватель музыки -->
      <div class="music-player mb-12">
        <h3 class="text-4xl font-semibold mb-6 text-center subtitle-styling">Слушайте треки артиста</h3>
        <div class="player-container">
          <audio controls class="audio-styling">
            <source src="https://example.com/path-to-song.mp3" type="audio/mpeg">
            Ваш браузер не поддерживает аудио-проигрыватель.
          </audio>
        </div>
      </div>

      <!-- Видеопроигрыватель с локальным видео и превью -->
      <div class="video-player mb-12">
        <h3 class="text-4xl font-semibold mb-6 text-center subtitle-styling">Смотрите демо-клип</h3>
        <div class="video-container">
          <video
            controls
            width="100%"
            height="400"
            poster="@/assets/img/preview-2.jpg"
            class="video-styling"
          >
            <source src="" type="video/mp4">
            Ваш браузер не поддерживает видео.
          </video>
        </div>
      </div>

      <!-- Галерея фотографий -->
      <div class="gallery">
        <h3 class="text-4xl font-semibold mb-6 text-center subtitle-styling">Фотографии с концертов и закулисных съемок</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
          <div v-for="(image, index) in galleryImages" :key="index" class="gallery-item">
            <img :src="image.src" :alt="image.alt" class="gallery-img hover:scale-105 transition-transform duration-500">
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MediaContent',
  data() {
    return {
      galleryImages: [
        { src: '@/assets/img/photo1.jpg', alt: 'Концерт артиста в Лондоне' },
        { src: '@/assets/img/preview-2.jpg', alt: 'Закулисные съемки клипа' },
        { src: '@/assets/img/photo3.jpg', alt: 'Выступление на фестивале' },
        { src: '@/assets/img/photo4.jpg', alt: 'Работа в студии над новым альбомом' },
        { src: '@/assets/img/photo5.jpg', alt: 'Вечер с поклонниками' },
        { src: '@/assets/img/photo6.jpg', alt: 'Закулисные моменты перед концертом' }
      ]
    };
  }
};
</script>

<style scoped>
.media-content {
  background-color: #1a1a1a;
  color: #e0e0e0;
  padding-bottom: 4rem;
  padding-top: 4rem;
}

.title-styling {
  font-family: 'Courier New', monospace;
  color: #ff0054;
  text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.6);
  letter-spacing: 0.2em;
  transform: rotate(-1deg);
}

.subtitle-styling {
  color: #ff0054;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  letter-spacing: 0.1em;
  font-family: 'Courier New', monospace;
}

.audio-styling {
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
  border-radius: 10px;
  background-color: #333;
  padding: 15px;
  border: 2px solid #ff0054;
}

.video-styling {
  border: 5px solid #ff0054;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
  transition: box-shadow 0.3s ease, transform 0.3s ease;
}

.video-styling:hover {
  box-shadow: 0 12px 40px rgba(255, 0, 84, 0.6);
  transform: scale(1.02);
}

.gallery-img {
  object-fit: cover;
  border: 4px solid #ff0054;
  border-radius: 12px;
}

.gallery-item:hover .gallery-img {
  transform: rotate(4deg) scale(1.05);
}

h2, h3 {
  color: #ff0054;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}
</style>
