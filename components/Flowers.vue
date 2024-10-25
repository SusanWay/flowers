<template>
  <div class="background">
    <div
        class="falling-flowers"
        v-for="index in flowerCount"
        :key="index"
        :style="{
        left: getRandomPosition(),
        animationDuration: getRandomDuration(),
        animationDelay: getRandomDelay()
      }"
    >
      {{ getRandomFlower() }}
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Количество падающих цветов
const flowerCount = 100;

// Массив с эмодзи цветов
const flowers = ['🌸', '🌼', '🌺', '💐'];

// Функция для получения случайной позиции по горизонтали
const getRandomPosition = () => {
  return Math.random() * 100 + 'vw'; // случайная позиция по горизонтали
};

// Функция для получения случайной продолжительности анимации
const getRandomDuration = () => {
  return Math.random() * 3 + 2 + 's'; // случайная продолжительность от 2 до 5 секунд
};

// Функция для получения случайной задержки анимации
const getRandomDelay = () => {
  return Math.random() * 5 + 's'; // случайная задержка от 0 до 5 секунд
};

// Функция для получения случайного цветка из массива
const getRandomFlower = () => {
  return flowers[Math.floor(Math.random() * flowers.length)];
};
</script>

<style scoped>
.background {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}

.falling-flowers {
  position: absolute;
  font-size: 2rem; /* Размер эмодзи */
  animation: fall linear infinite; /* Бесконечная анимация падения */

  /* Скрытие цветков до начала анимации */
  opacity: 0; /* Начальная прозрачность */
}

@keyframes fall {
  from {
    top: -10%;
    opacity: 1; /* Полная видимость при начале анимации */
    visibility: visible; /* Делаем видимыми при начале падения */
  }

  to {
    top: 100%;
    opacity: 0; /* Уменьшение прозрачности при падении */
    visibility: hidden; /* Скрытие после завершения анимации */
  }
}
</style>