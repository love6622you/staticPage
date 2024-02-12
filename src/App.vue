<template>
  <div class="flex h-[100dvh] flex-col md:flex-row">
    <!-- According to breakpoint render -->
    <Sidebar class="hidden md:flex" />
    <MobileNav class="flex md:hidden" />

    <div class="flex-1 bg-[#DCCCBC]">content</div>
  </div>
</template>

<script setup>
import MobileNav from './components/Layout/MobileNav.vue';
import Sidebar from './components/Layout/Sidebar.vue';
</script>

<style scoped></style>
