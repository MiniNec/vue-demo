<script setup lang="ts">
import Glass from '@/components/Glass.vue';
import Chance from '@/components/Chance.vue';
import Square from '@/components/Square.vue';
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
      <square rDeg="0" text="世界杯" color="pink"></square>
      <glass rDeg="0" text="布拉格" color="green"></glass>
      <glass rDeg="0" text="普吉岛" color="green"></glass>
      <glass rDeg="0" text="柏林" color="red"></glass>
      <chance rDeg="0" text="机会" color="red"></chance>
      <glass rDeg="0" text="莫斯科" color="red"></glass>
      <glass rDeg="0" text="日内瓦" color="green"></glass>
      <glass rDeg="0" text="罗马" color="green"></glass>
      <square rDeg="0" text="世界旅游" color="pink"></square>
    </div>
  </div>
</template>

<style scoped>
.container {
  position: relative;
  width: 1740px;
  height: 1000px;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.5s;
  border-radius: 10px;
  background: #000;
}
</style>
