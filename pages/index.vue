<script setup lang="ts">

import Flowers from "~/components/Flowers.vue";
</script>

<template>
  <div class="w-full h-[100vh]">
    <Flowers/>
    <div class="bg-white/10 sm:bg-white/30 absolute flex flex-col justify-center sm:block left-0 right-0 top-0 bottom-0 sm:bottom-auto sm:right-auto text-white py-2 px-4 md:py-4 md:px-12 sm:top-[50%] sm:left-[50%] sm:translate-x-[-50%] sm:translate-y-[-50%] sm:rounded-2xl">
      <p class="text-xl sm:text-title font-sans font-bold text-center">
        Поздравляю с днем Дня!
      </p>
      <img class="mx-auto" src="https://i.ibb.co/1MJV1rB/cats.png" alt="">
      <p class="text-xl sm:text-title-sm  md:text-title font-sans font-bold text-center">
        Для моей любимой <span> Кринжули 😎</span>
      </p>
    </div>
  </div>
</template>

<style scoped>

</style>