<template>
  <div class="spec-glass" :style="spec_style" :data-text="props.money">
    <i>{{ props.text }}</i>
    <!-- <player class="spec-player"></player> -->
  </div>
</template>

<script setup lang="ts">
import player from '@/components/Player.vue';
const props = defineProps<{
  //rDeg: number;
  text: string;
  //money: number;
  color: string;
}>();
// const spec_style = '--r:' + props.rDeg + '; --color:' + props.color;
const spec_style = '--color:' + props.color;
</script>

<style scoped>
.spec-glass {
  position: relative;
  width: 240px;
  height: 240px;
  background: var(--color);
  /* background: linear-gradient(var(--color), transparent); */
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 25px 25px rgba(0, 0, 0, 0.25);
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.5s;
  border-radius: 10px;
  /* transform: rotate(calc(var(--r) * 1deg)); */
  box-sizing: border-box;
}
.spec-glass:hover {
  transform: translate(-20px, -20px);
}

.spec-glass::before {
  content: attr(data-text);
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 40px;
  background: rgba(255, 255, 255, 0.05);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  font-size: 25px;
}

.spec-glass i {
  font-size: 3em;
  color: #000;
  font-weight: border;
}

.spec-player {
  display: flex;
  scale: 0.5;
  margin-left: -160px;
  transform: skew(20deg, 10deg) rotate(-30deg);
}
</style>
