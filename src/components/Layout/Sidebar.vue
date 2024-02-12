<template>
  <div class="relative basis-[375px] bg-white">
    <Logo class="absolute left-full top-[40px] z-10 h-[100px] w-[100px] -translate-x-[50px]" />
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
