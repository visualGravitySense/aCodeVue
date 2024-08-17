<template>
  <section class="contact-section py-16 px-4">
    <div class="container mx-auto">
      <!-- Заголовок -->
      <h2 class="text-5xl font-bold text-center mb-12 title-styling">Форма обратной связи</h2>

      <!-- Форма обратной связи -->
      <form @submit.prevent="submitForm" class="max-w-lg mx-auto bg-dark-gray p-8 rounded-lg shadow-lg">
        <div class="mb-6">
          <label for="name" class="block text-xl font-bold mb-2 label-styling">Имя</label>
          <input v-model="form.name" type="text" id="name" placeholder="Введите ваше имя" required class="w-full px-4 py-3 border border-dark-gray rounded-lg bg-gray-900 text-light-gray placeholder-gray-500" />
        </div>
        
        <div class="mb-6">
          <label for="email" class="block text-xl font-bold mb-2 label-styling">Email</label>
          <input v-model="form.email" type="email" id="email" placeholder="Введите ваш email" required class="w-full px-4 py-3 border border-dark-gray rounded-lg bg-gray-900 text-light-gray placeholder-gray-500" />
        </div>

        <div class="mb-6">
          <label for="message" class="block text-xl font-bold mb-2 label-styling">Сообщение</label>
          <textarea v-model="form.message" id="message" rows="5" placeholder="Введите ваше сообщение" required class="w-full px-4 py-3 border border-dark-gray rounded-lg bg-gray-900 text-light-gray placeholder-gray-500"></textarea>
        </div>

        <div class="mb-6 flex items-center">
          <input v-model="form.subscribe" type="checkbox" id="subscribe" class="mr-3 accent-pink-500" />
          <label for="subscribe" class="text-xl font-semibold text-light-gray">Подписаться на рассылку</label>
        </div>

        <button type="submit" class="w-full bg-pink-600 text-white py-3 px-6 rounded-lg hover:bg-pink-500 transition-colors duration-300">
          Отправить
        </button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactForm',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: '',
        subscribe: false
      }
    };
  },
  methods: {
    submitForm() {
      // Логика отправки формы
      // Можно использовать API или email-сервис для отправки данных

      console.log('Форма отправлена:', this.form);

      // Очистка формы после отправки
      this.form.name = '';
      this.form.email = '';
      this.form.message = '';
      this.form.subscribe = false;
      
      alert('Ваше сообщение отправлено! Спасибо за вашу поддержку.');
    }
  }
};
</script>

<style scoped>
.contact-section {
  background-color: #121212;
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

.bg-dark-gray {
  background-color: #1e1e1e;
}

.label-styling {
  color: #ff007f;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

input, textarea {
  border: 1px solid #333;
  background-color: #1e1e1e;
  color: #e0e0e0;
}

button {
  transition: background-color 0.3s ease, transform 0.2s ease;
}

button:hover {
  background-color: #e60073;
  transform: scale(1.05);
}
</style>
