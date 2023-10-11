<template>
  <div class="spec-glass" :style="spec_style" :data-text="multiple">
    <i>{{ props.text }}</i>
    <div v-if="display_house1" class="spec-house spec-house1">房1</div>
    <div v-if="display_house2" class="spec-house spec-house2">房2</div>
    <div v-if="display_house3" class="spec-house spec-house3">房3</div>
    <div v-if="display_house4" class="spec-house spec-house4">Big房</div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const props = defineProps<{
  text: string;
  color: string;
}>();
// const spec_style = '--r:' + props.rDeg + '; --color:' + props.color;
const spec_style = ' --color:' + props.color;

/* 小房子展示 */
const display_house1 = ref(false);
const display_house2 = ref(false);
const display_house3 = ref(false);
const display_house4 = ref(false);

/* 下方小字绑定值 */
const multiple = ref('X1');

/* 买了房子的小房子展示 */
const showHouse = (num: number) => {
  if (num == 0) {
    display_house1.value = false;
    display_house2.value = false;
    display_house3.value = false;
    display_house4.value = false;
  } else if (num == 1) {
    display_house1.value = true;
  } else if (num == 2) {
    display_house1.value = true;
    display_house2.value = true;
  } else if (num == 3) {
    display_house1.value = true;
    display_house2.value = true;
    display_house3.value = true;
  } else if (num == 4) {
    display_house1.value = false;
    display_house2.value = false;
    display_house3.value = false;
    display_house4.value = true;
  }
};

/* 设置下方倍数小字 */
const setMultiple = (str: string) => {
  multiple.value = str;
};

defineExpose({
  showHouse,
  setMultiple,
});
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
  /* transform: rotate(calc(var(--r) * 1deg)); */
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
  color: #fff;
  transform: rotate(-90deg);
}
</style>
