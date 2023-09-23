<script setup lang="ts">
defineProps<{ name: string }>();
</script>

<template>
  <ul>
    <li>
      <a>{{ name }}</a>
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
  transform: skewY(-30deg);
  z-index: var(--i);
}

ul li {
  position: relative;
  list-style: none;
  width: 80px;
  background: #eeeeee;
  padding: 15px;
  transition: 0.5s;
  transform: skewX(45deg);
  height: 100px;
}

ul li:hover {
  background: #33a3ee;
}

ul li:hover::before {
  background: #33a3ee;
}

ul li:hover::after {
  background: #33a3ee;
}

ul li::before {
  content: '';
  position: absolute;
  top: 0px;
  left: -10px;
  width: 10px;
  height: 100px;
  background: #eeeeff;
  transform-origin: right;
  transform: skewY(-45deg);
  transition: 0.5s;
}

ul li::after {
  content: '';
  position: absolute;
  top: 100px;
  left: -10px;
  width: 80px;
  height: 10px;
  background: #eeeeff;
  transform-origin: bottom;
  transform: skewX(-45deg);
  transition: 0.5s;
}

ul li a {
  text-decoration: none;
  color: #999;
  display: block;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  transition: 0.5s;
  font-size: 15px;
}

ul li:hover a {
  color: #fff;
}
</style>
