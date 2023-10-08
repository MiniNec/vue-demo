<script setup lang="ts">
import glass from '@/components/Glass.vue';
import lGlass from '@/components/LGlass.vue';
import chance from '@/components/Chance.vue';
import lChance from '@/components/LChance.vue';
import lBank from '@/components/LBank.vue';
import square from '@/components/Square.vue';
</script>

<template>
  <div class="container">
    <square
      style="position: absolute; top: 0px; left: 0px"
      rDeg="0"
      text="世界杯"
      color="pink"
    ></square>
    <glass
      style="position: absolute; top: 0px; left: 240px"
      rDeg="0"
      text="布拉格"
      color="#DE4BF4"
    ></glass>
    <glass
      style="position: absolute; top: 0px; left: 420px"
      rDeg="0"
      text="普吉岛"
      color="#8AE2D5"
    ></glass>
    <glass
      style="position: absolute; top: 0px; left: 600px"
      rDeg="0"
      text="柏林"
      color="#DE4BF4"
    ></glass>
    <chance
      style="position: absolute; top: 0px; left: 780px"
      rDeg="0"
      text="机会"
      color="#E8EDE8"
    ></chance>
    <glass
      style="position: absolute; top: 0px; left: 960px"
      rDeg="0"
      text="莫斯科"
      color="#9603AD"
    ></glass>
    <glass
      style="position: absolute; top: 0px; left: 1140px"
      rDeg="0"
      text="日内瓦"
      color="#9603AD"
    ></glass>
    <glass
      style="position: absolute; top: 0px; left: 1320px"
      rDeg="0"
      text="罗马"
      color="#9603AD"
    ></glass>
    <square
      style="position: absolute; top: 0px; left: 1500px"
      rDeg="0"
      text="世界旅游"
      color="pink"
    ></square>
    <lGlass
      style="position: absolute; top: 240px; left: 0px"
      text="圣保罗"
      color="blue"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 420px; left: 0px"
      text="夏威夷"
      color="#8AE2D5"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 600px; left: 0px"
      text="魁北克"
      color="blue"
    ></lGlass>
    <lChance
      style="position: absolute; top: 780px; left: 0px"
      text="机会"
      color="#E8EDE8"
    ></lChance>
    <lGlass
      style="position: absolute; top: 960px; left: 0px"
      text="悉尼"
      color="#3498DB"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 1140px; left: 0px"
      text="东京"
      color="#3498DB"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 1320px; left: 0px"
      text="巴厘岛"
      color="#8AE2D5"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 240px; left: 1500px"
      text="塔希提岛"
      color="#8AE2D5"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 420px; left: 1500px"
      text="伦敦"
      color="#ED954E"
    ></lGlass>
    <lGlass
      style="position: absolute; top: 600px; left: 1500px"
      text="巴黎"
      color="#ED954E"
    ></lGlass>
    <lChance
      style="position: absolute; top: 780px; left: 1500px"
      text="机会"
      color="#E8EDE8"
    ></lChance>
    <lGlass
      style="position: absolute; top: 960px; left: 1500px"
      text="纽约"
      color="#ED1717"
    ></lGlass>
    <lBank
      style="position: absolute; top: 1140px; left: 1500px"
      text="国税局"
      color="#E8EDE8"
    ></lBank>
    <lGlass
      style="position: absolute; top: 1320px; left: 1500px"
      text="北京"
      color="#ED1717"
    ></lGlass>
    <square
      style="position: absolute; top: 1500px; left: 0px"
      rDeg="0"
      text="无人岛"
      color="pink"
    ></square>
    <glass
      style="position: absolute; top: 1500px; left: 240px"
      rDeg="0"
      text="开罗"
      color="#2EC12E"
    ></glass>
    <glass
      style="position: absolute; top: 1500px; left: 420px"
      rDeg="0"
      text="迪拜"
      color="#2EC12E"
    ></glass>
    <glass
      style="position: absolute; top: 1500px; left: 600px"
      rDeg="0"
      text="新德里"
      color="#2EC12E"
    ></glass>
    <glass
      style="position: absolute; top: 1500px; left: 780px"
      rDeg="0"
      text="马尔代夫"
      color="#8AE2D5"
    ></glass>
    <glass
      style="position: absolute; top: 1500px; left: 960px"
      rDeg="0"
      text="首尔"
      color="#00FF00"
    ></glass>
    <chance
      style="position: absolute; top: 1500px; left: 1140px"
      rDeg="0"
      text="奖励"
      color="#E8EDE8"
    ></chance>
    <glass
      style="position: absolute; top: 1500px; left: 1320px"
      rDeg="0"
      text="曼谷"
      color="#00FF00"
    ></glass>
    <square
      style="position: absolute; top: 1500px; left: 1500px"
      rDeg="0"
      text="起点"
      color="pink"
    ></square>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  position: relative;
  /* justify-content: center; */
  /* align-items: center; */
  /* scale: 0.8; */
  width: 1740px;
  height: 1740px;
  scale: 0.5;
}
</style>
