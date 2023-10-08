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
      style="position: absolute; top: 10px; left: 10px"
      rDeg="0"
      text="1"
      color="pink"
    ></square>
    <glass
      style="position: absolute; top: 10px; left: 10px"
      rDeg="0"
      text="2"
      color="#DE4BF4"
    ></glass>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  position: relative;
  /* justify-content: center; */
  /* align-items: center; */
  /* scale: 0.8; */
  width: 1000px;
  height: 1000px;
}
</style>
