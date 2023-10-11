<template>
  <div class="spec-glass" :style="spec_style" :data-text="props.money">
    <i>{{ props.text }}</i>
    <div v-if="display_house1" class="spec-house spec-house1">房1</div>
    <div v-if="display_house2" class="spec-house spec-house2">房2</div>
    <div v-if="display_house3" class="spec-house spec-house3">房3</div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const props = defineProps<{
  rDeg: number;
  text: string;
  money: number;
  color: string;
}>();
const spec_style = '--r:' + props.rDeg + '; --color:' + props.color;

const display_house1 = ref(false);
const display_house2 = ref(false);
const display_house3 = ref(false);

const showHouse = (num: number) => {
  if (num == 0) {
    display_house1.value = false;
    display_house2.value = false;
    display_house3.value = false;
  } else if (num == 1) {
    display_house1.value = true;
  } else if (num == 2) {
    display_house1.value = true;
    display_house2.value = true;
  } else if (num == 3) {
    display_house1.value = true;
    display_house2.value = true;
    display_house3.value = true;
  }
};

defineExpose({
  showHouse,
});
</script>

<style scoped>
.spec-glass {
  position: relative;
  width: 180px;
  height: 240px;
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
  color: #fff;
}

.spec-house {
  position: absolute;
  height: 30px;
  width: 30px;
  top: 50px;
  left: 20px;
  background-color: #fff;
}

.spec-house1 {
  left: 20px;
}

.spec-house2 {
  left: 70px;
}

.spec-house3 {
  left: 120px;
}
</style>
