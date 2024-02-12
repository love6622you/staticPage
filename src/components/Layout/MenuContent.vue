<template>
  <ul class="flex flex-col gap-y-5 text-center">
    <li
      v-for="menu in menuList"
      :key="menu.key"
      class="cursor-pointer transition-colors duration-300 ease-out hover:text-[#AA6666]"
      :class="selected === menu.key ? 'selected' : ''"
      @click="handleClick(menu.key)"
    >
      {{ menu.label }}
    </li>
  </ul>
</template>

<script setup>
const menuList = [
  { key: 'feature', label: '白頭翁的特性', link: '#feature' },
  { key: 'stories', label: '白頭翁的故事', link: '#stories' },
  { key: 'photos', label: '白頭翁的美照', link: '#photos' },
  { key: 'crisis', label: '白頭翁的危機', link: '#crisis' },
];

import { ref } from 'vue';
const selected = ref(menuList[0].key);
const handleClick = (value) => {
  selected.value = value;
};
</script>

<style scoped>
.selected {
  @apply font-bold text-[#AA6666] underline;
}
</style>
