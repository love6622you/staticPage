<template>
  <div
    class="h-[50px] w-[50px] rounded-full bg-white shadow-md shadow-black/25 md:h-[100px] md:w-[100px]"
  >
    <div class="relative h-full">
      <span class="body"></span>
      <span class="eye"></span>
      <span class="beak"></span>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.body {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 40%;
  height: 40%;
  background-color: black;
  border-top-left-radius: 50px;
  border-top-right-radius: 30px;
  border-bottom-right-radius: 30px;

  &::before {
    content: '';
    position: absolute;
    top: 50%;
    left: -5%;
    transform: translate(0, -50%);
    width: 105%;
    height: 60%;
    background-color: white;
    border-top-left-radius: 100px;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 50px;
  }
}
.eye {
  position: absolute;
  top: 50%;
  right: 50%;
  transform: translate(150%, -50%);
  width: 8%;
  height: 8%;
  background-color: black;
  border-radius: 50%;
}
.beak {
  position: absolute;
  top: 40%;
  right: 19%;
  width: 12%;
  height: 6%;
  border-radius: 0% 100% 0 0;
  background-color: black;
  transform: skew(10deg, -10deg);
}
</style>
