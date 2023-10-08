<template>
  <div class="spec-glass" :style="spec_style" :data-text="props.money">
    <i
      ><div>{{ props.text }}</div>
      <div>
        <el-icon style="vertical-align: middle; font-size: 2em"
          ><star
        /></el-icon>
      </div>
    </i>
  </div>
</template>

<script setup lang="ts">
import { Star } from '@element-plus/icons-vue';
const props = defineProps<{
  rDeg: number;
  text: string;
  money: number;
  color: string;
}>();
const spec_style = '--r:' + props.rDeg + '; --color:' + props.color;
</script>

<style scoped>
.spec-glass {
  position: relative;
  width: 240px;
  height: 180px;
  background: var(--color);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 25px 25px rgba(0, 0, 0, 0.25);
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.5s;
  border-radius: 10px;
  transform: rotate(calc(var(--r) * 1deg));
  box-sizing: border-box;
}
.spec-glass:hover {
  transform: translate(-10px, -10px);
}

.spec-glass::before {
  content: attr(data-text);
  position: absolute;
  bottom: 0;
  width: 183px;
  height: 40px;
  right: -70px;
  top: 69px;
  background: rgba(255, 255, 255, 0.05);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  font-size: 25px;
  transform: rotate(-90deg);
}

.spec-glass i {
  font-size: 3em;
  color: #000;
  transform: rotate(-90deg);
}
</style>
