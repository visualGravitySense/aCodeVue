<template>
  <section class="project-description py-16 px-4">
    <div class="container mx-auto">
      <!-- Краткая история артиста -->
      <div class="mb-12 anti-style-block">
        <h2 class="text-3xl font-bold mb-4 uppercase border-b-4 pb-2 border-yellow-500">Краткая история артиста</h2>
        <p class="text-lg leading-relaxed">
          {{ artistHistory }}
        </p>
      </div>

      <!-- Цель кампании -->
      <div class="mb-12 anti-style-block">
        <h2 class="text-3xl font-bold mb-4 uppercase border-b-4 pb-2 border-red-500">Цель кампании</h2>
        <p class="text-lg leading-relaxed">
          {{ campaignGoal }}
        </p>
      </div>

      <!-- Отличия проекта -->
      <div class="anti-style-block">
        <h2 class="text-3xl font-bold mb-4 uppercase border-b-4 pb-2 border-blue-500">Отличия проекта</h2>
        <p class="text-lg leading-relaxed">
          {{ projectUniquePoints }}
        </p>
      </div>
    </div>
  </section>
</template>
  
  <script>
  export default {
    name: 'ProjectDescription',
    data() {
      return {
        artistHistory: `Артист начал свой путь в музыкальной индустрии в начале 2000-х годов. Его стиль вдохновлен классическим британским роком, с элементами блюза и психоделии. С тех пор он выпустил несколько альбомов и завоевал признание за свои мощные выступления и уникальное звучание.`,
        campaignGoal: `Цель этой кампании — собрать 50 000 долларов на создание нового клипа, который будет сочетать в себе элементы живого выступления и креативного повествования. Эти средства помогут покрыть расходы на съемку, монтаж и продвижение клипа.`,
        projectUniquePoints: `Этот клип выделяется тем, что он будет создан в сотрудничестве с известным режиссером и командой художников. В проекте будут использованы уникальные визуальные эффекты и интерактивные элементы, которые не были использованы в предыдущих работах артиста. Поддержка этого проекта поможет создать нечто совершенно новое и захватывающее.`
      }
    }
  }
  </script>
  
  <style scoped>
  .project-description {
  background-color: #000; /* Чёрный фон для контраста */
  color: #e1e1e1; /* Светлый текст */
  font-family: 'Courier New', Courier, monospace; /* Грубая типографика */
  text-transform: uppercase; /* Британская сдержанность с индустриальным стилем */
  letter-spacing: 2px;
}

.anti-style-block {
  background-color: #111; /* Тёмный блок для секций */
  padding: 2rem;
  margin-bottom: 2rem;
  border: 5px solid transparent; /* Ожидаемый цвет задаётся у заголовка */
  transition: transform 0.3s, border-color 0.3s;
}

.anti-style-block:hover {
  transform: rotate(-2deg) scale(1.05); /* Анимация вращения при наведении */
  border-color: #fff; /* Изменение цвета границы при наведении */
}

.project-description h2 {
  color: #fff; /* Белые заголовки */
  background-color: #111; /* Темный фон для заголовков */
  padding: 1rem 0;
  text-align: left;
  font-size: 2.5rem; /* Смелая типографика */
  position: relative;
}

.project-description p {
  font-size: 1.25rem; /* Крупный текст */
  margin-bottom: 1rem;
  line-height: 1.8;
  color: #aaa; /* Смягчённый цвет для текста */
}

.border-b-4 {
  display: inline-block;
}

.border-yellow-500 {
  border-color: #f1c40f;
}

.border-red-500 {
  border-color: #e74c3c;
}

.border-blue-500 {
  border-color: #3498db;
}

  </style>