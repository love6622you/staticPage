<template>
  <div class="rounded-full shadow-md shadow-black/25">
    <div class="relative">
      <div class="beak"></div>
      <div class="eye"></div>
      <div class="head"></div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.beak {
  width: 20px;
  height: 10px;
  background-color: red;
  position: absolute;
  top: 50%;
  left: 40%;
  transform-origin: top left;
  transform: rotate(-45deg);
}

.eye {
  width: 10px;
  height: 10px;
  background-color: red;
  position: absolute;
  top: 40%;
  left: 60%;
  border-radius: 50%;
}

.head {
  width: 80px;
  height: 80px;
  background-color: red;
  position: absolute;
  top: 10%;
  left: 10%;
  border-radius: 50%;
}
</style>
