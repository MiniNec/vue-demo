<script setup lang="ts">
import Glass from '@/components/Glass.vue';
import LGlass from '@/components/LGlass.vue';
import Chance from '@/components/Chance.vue';
import Square from '@/components/Square.vue';
import Player from '@/components/Player.vue';
</script>

<template>
  <div
    style="
      display: flex;
      width: 2200px;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      scale: 1;
    "
  >
    <div class="container" style="width: 1767px; height: 1767px; scale: 0.3">
      <square rDeg="0" text="世界杯" color="pink"></square>
      <glass rDeg="0" text="布拉格" color="green"></glass>
      <glass rDeg="0" text="普吉岛" color="green"></glass>
      <glass rDeg="0" text="柏林" color="red"></glass>
      <chance rDeg="0" text="机会" color="red"></chance>
      <glass rDeg="0" text="莫斯科" color="red"></glass>
      <glass rDeg="0" text="日内瓦" color="green"></glass>
      <glass rDeg="0" text="罗马" color="green"></glass>
      <square rDeg="0" text="世界旅游" color="pink"></square>
      <div style="width: 243px">
        <lGlass text="圣保罗" color="blue" money="123"></lGlass>
        <lGlass text="夏威夷" color="#A3E4D7"></lGlass>
        <lGlass text="魁北克" color="blue"></lGlass>
        <lGlass text="机会" color="red"></lGlass>
        <lGlass text="悉尼" color="#3498DB"></lGlass>
        <lGlass text="东京" color="#3498DB"></lGlass>
        <lGlass text="巴厘岛" color="#A3E4D7"></lGlass>
      </div>
      <div style="width: 1279px; color: #fff">1231232s12414</div>
      <div style="width: 243px">
        <lGlass text="圣保罗" color="blue"></lGlass>
        <lGlass text="夏威夷" color="#A3E4D7"></lGlass>
        <lGlass text="魁北克" color="blue"></lGlass>
        <lGlass text="机会" color="red"></lGlass>
        <lGlass text="悉尼" color="#3498DB"></lGlass>
        <lGlass text="东京" color="#3498DB"></lGlass>
        <lGlass text="巴厘岛" color="#A3E4D7"></lGlass>
      </div>
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
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
  transition: 0.5s;
  border-radius: 10px;
  background: #000;
  transform: rotate(30deg) skew(-20deg, -10deg);
}
</style>
