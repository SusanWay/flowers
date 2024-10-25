<script setup lang="ts">

import Flowers from "~/components/Flowers.vue";
</script>

<template>
  <div class="w-full h-[100vh]">
    <Flowers/>
    <div class="bg-white/30 absolute text-white top-[50%] py-4 px-12 left-[50%] translate-x-[-50%] translate-y-[-50%] rounded-2xl ">
      <p class="text-title font-sans font-bold text-center">
        Поздравляю с днем Дня!
      </p>
      <img class="mx-auto" src="https://i.ibb.co/1MJV1rB/cats.png" alt="">
      <p class="text-title font-sans font-bold ">
        Для моей любимой <span> Кринжули 😎</span>
      </p>
    </div>
  </div>
</template>

<style scoped>

</style>