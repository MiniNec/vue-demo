<script setup lang="ts">
import Demo from '@/components/Demo.vue';
import LPlace from '@/components/LPlace.vue';
import SPlace from '@/components/SPlace.vue';
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
    <sPlace name="123"></sPlace>
    <!-- <lPlace name="1" style="--i: 9"></lPlace>
    <lPlace name="2" style="--i: 8; margin-bottom: 90px"></lPlace>
    <lPlace name="3" style="--i: 7; margin-bottom: 180px"></lPlace>
    <lPlace name="4" style="--i: 6; margin-bottom: 270px"></lPlace>
    <lPlace name="5" style="--i: 5; margin-bottom: 360px"></lPlace>
    <lPlace name="6" style="--i: 4; margin-bottom: 450px"></lPlace>
    <lPlace name="7" style="--i: 3; margin-bottom: 540px"></lPlace> -->
  </div>
</template>

<style scoped></style>
