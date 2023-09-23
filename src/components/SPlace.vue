<script setup lang="ts">
defineProps<{ name: string }>();
</script>

<template>
  <ul>
    <li>
      <a>{{ name }}</a>
      <zz></zz>
      <zz></zz>
    </li>
  </ul>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Oswald', sans-serif;
}

ul {
  position: relative;
  transform: ;
  z-index: var(--i);
  transform: rotate(45deg);
}

ul li {
  position: relative;
  list-style: none;
  width: 100px;
  height: 100px;
  background: #eeeeee;
  padding: 15px;
  z-index: var(--i);
  transition: 0.5s;
}

ul li:hover {
  background: #33a3ee;
}

ul li a {
  text-decoration: none;
  color: #999;
  display: block;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  transition: 0.5s;
  transform: rotate(-45deg);
}
</style>
