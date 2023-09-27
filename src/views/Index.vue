<script setup lang="ts">
import Glass from '@/components/Glass.vue';
</script>

<template>
  <div
    style="
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      scale: 1;
    "
  >
    <div class="container">
      <glass rDeg="0" text="镇江" money="¥500" color="green"></glass>
      <glass rDeg="0" text="南京" money="¥500" color="green"></glass>
      <glass rDeg="0" text="日本" money="¥500" color="red"></glass>
      <glass rDeg="0" text="镇江" money="¥500" color="red"></glass>
      <glass rDeg="0" text="南京" money="¥500" color="red"></glass>
      <glass rDeg="0" text="日本" money="¥500" color="green"></glass>
    </div>
  </div>
</template>

<style scoped>
.container {
  position: relative;
  width: 1000px;
  height: 1000px;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.5s;
  border-radius: 10px;
  background: #000;
}
</style>
