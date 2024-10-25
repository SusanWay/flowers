<script setup lang="ts">
</script>

<template>
  <div class="mx-auto flex h-full min-h-screen max-w-[2560px] flex-col">
    <LayoutHeader />
    <div class="flex-auto bg-[#1c1938]">
      <slot />
    </div>
    <LayoutFooter/>
  </div>
</template>
