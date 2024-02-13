<template>
  <nav class="fixed z-30 w-full bg-white shadow-md">
    <div class="flex w-full items-center justify-between px-6 py-[1.875rem]">
      <div>
        <input id="menu" v-model="open" type="checkbox" class="hidden" />
        <label for="menu" class="space-y-2">
          <span
            class="block h-1 w-6 bg-black transition-transform ease-in-out"
            :class="{ ['translate-y-1.5 rotate-45']: open }"
          ></span>
          <span v-if="!open" class="block h-1 w-4 bg-black transition-transform ease-in-out"></span>
          <span
            class="block h-1 w-6 bg-black transition-transform ease-in-out"
            :class="{ ['-translate-y-1.5 -rotate-45']: open }"
          ></span>
        </label>
      </div>

      <h3 class="text-xl font-bold">白頭翁不吃小米</h3>
      <Logo />
    </div>

    <MenuContent v-show="open" />
  </nav>
</template>

<script setup>
import { ref } from 'vue';
import Logo from '../Logo.vue';
import MenuContent from './MenuContent.vue';

const open = ref(false);
</script>

<style scoped></style>
