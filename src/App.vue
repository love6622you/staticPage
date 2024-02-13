<template>
  <div class="flex h-dvh flex-col overflow-hidden md:flex-row">
    <!-- According to breakpoint render -->
    <Sidebar class="hidden md:flex" />
    <MobileNav class="block md:hidden" />

    <main class="mt-[88px] flex-1 overflow-y-auto bg-[#DCCCBC] md:mt-0">
      <section>
        <div class="banner_hero">
          <div class="absolute bottom-9 right-10 space-y-2 text-right text-white">
            <h1 class="ml-auto w-72 text-5xl font-bold md:w-auto">白頭翁 (Chinese bulbul)</h1>
            <p class="ml-auto w-auto pl-10 text-lg">
              又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10 年。
            </p>
          </div>
        </div>

        <ul
          :class="['flex flex-col gap-12 px-9 py-12', 'md:gap-20 md:px-12 md:py-14', 'lg:flex-row']"
        >
          <li v-for="item in featureList" :key="item.key" class="flex flex-1 gap-x-9">
            <h2 class="title_circle relative h-fit text-4xl font-bold">{{ item.title }}</h2>
            <p>{{ item.content }}</p>
          </li>
        </ul>
      </section>
    </main>
  </div>
</template>

<script setup>
const featureList = [
  {
    key: 'Appearance',
    title: '外觀',
    content:
      '白頭鵯體長約17到22公分，額至頭頂純黑色而富有光澤，兩眼上方至後枕白色，形成一白色枕環。耳羽後部有一白斑，此白環與白斑在黑色的頭部均極為醒目，老鳥的枕羽(後頭部)更潔白，所以又叫「白頭翁」。',
  },
  {
    key: 'Habitat',
    title: '棲地',
    content:
      '白頭翁和麻雀、綠繡眼合稱「城市三寶」，常成群出現在平原區灌木叢、丘陵樹林地帶，以及校園、公園、庭院、行道中的各種高高的電線與樹上。',
  },
  {
    key: 'Food Habit',
    title: '食性',
    content:
      '以果樹的漿果和種子為主食，並時常飛入果園偷吃果實，還會吃嫩葉嫩芽，尤其是胡蝶蘭的嫩葉嫩芽葉，偶爾啄食昆蟲。',
  },
];

import MobileNav from './components/Layout/MobileNav.vue';
import Sidebar from './components/Layout/Sidebar.vue';
</script>

<style scoped>
.banner_hero {
  position: relative;
  height: clamp(40vh, 300px, 635px);
  background-image: url('./assets/images/Banner.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.title_circle::before {
  content: '';
  position: absolute;
  bottom: 0;
  right: -10px;
  width: 12px;
  height: 12px;
  box-shadow: 0 0 0 7.5px #aa6666;
  opacity: 0.6;
  border-radius: 50%;
}
</style>
