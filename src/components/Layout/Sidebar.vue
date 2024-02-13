<template>
  <div class="relative basis-[345px] bg-white">
    <div class="absolute left-full top-[40px] z-30 -translate-x-[50px]">
      <Logo />
    </div>

    <div class="mx-auto">
      <h2 class="my-[4.625rem] text-3xl font-bold">白頭翁不吃小米</h2>
      <MenuContent />
    </div>
  </div>
</template>

<script setup>
import MenuContent from './MenuContent.vue';
import Logo from '../Logo.vue';
</script>

<style scoped></style>
