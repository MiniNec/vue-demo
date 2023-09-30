<script setup lang="ts">
import glass from '@/components/Glass.vue';
import lGlass from '@/components/LGlass.vue';
import chance from '@/components/Chance.vue';
import lChance from '@/components/LChance.vue';
import lBank from '@/components/LBank.vue';
import square from '@/components/Square.vue';
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
      <glass rDeg="0" text="布拉格" color="#DE4BF4"></glass>
      <glass rDeg="0" text="普吉岛" color="#8AE2D5"></glass>
      <glass rDeg="0" text="柏林" color="#DE4BF4"></glass>
      <chance rDeg="0" text="机会" color="#E8EDE8"></chance>
      <glass rDeg="0" text="莫斯科" color="#9603AD"></glass>
      <glass rDeg="0" text="日内瓦" color="#9603AD"></glass>
      <glass rDeg="0" text="罗马" color="#9603AD"></glass>
      <square rDeg="0" text="世界旅游" color="pink"></square>
      <div style="width: 243px">
        <lGlass text="圣保罗" color="blue"></lGlass>
        <lGlass text="夏威夷" color="#8AE2D5"></lGlass>
        <lGlass text="魁北克" color="blue"></lGlass>
        <lChance text="机会" color="#E8EDE8"></lChance>
        <lGlass text="悉尼" color="#3498DB"></lGlass>
        <lGlass text="东京" color="#3498DB"></lGlass>
        <lGlass text="巴厘岛" color="#8AE2D5"></lGlass>
      </div>
      <div style="width: 1279px; color: #fff">1231232s12414</div>
      <div style="width: 243px">
        <lGlass text="塔希提岛" color="#8AE2D5"></lGlass>
        <lGlass text="伦敦" color="#ED954E"></lGlass>
        <lGlass text="巴黎" color="#ED954E"></lGlass>
        <lChance text="机会" color="#E8EDE8"></lChance>
        <lGlass text="纽约" color="#ED1717"></lGlass>
        <lBank text="国税局" color="#E8EDE8"></lBank>
        <lGlass text="北京" color="#ED1717"></lGlass>
      </div>
      <square rDeg="0" text="无人岛" color="pink"></square>
      <glass rDeg="0" text="开罗" color="#2EC12E"></glass>
      <glass rDeg="0" text="迪拜" color="#2EC12E"></glass>
      <glass rDeg="0" text="新德里" color="#2EC12E"></glass>
      <glass rDeg="0" text="马尔代夫" color="#8AE2D5"></glass>
      <glass rDeg="0" text="首尔" color="#00FF00"></glass>
      <chance rDeg="0" text="奖励" color="#E8EDE8"></chance>
      <glass rDeg="0" text="曼谷" color="#00FF00"></glass>
      <square rDeg="0" text="起点" color="pink"></square>
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
  background: #bcbcbc;
  transform: rotate(30deg) skew(-20deg, -10deg);
}
</style>
