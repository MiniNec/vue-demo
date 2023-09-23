<script setup lang="ts">
defineProps<{ name: string }>();
</script>

<template>
  <div>
    <ul>
      <li style="--i: 1">
        <a>{{ name }}</a>
      </li>
    </ul>
  </div>
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
  transform: skewY(-15deg);
}

ul li {
  position: relative;
  list-style: none;
  width: 100px;
  background: #eeeeee;
  padding: 15px;
  z-index: var(--i);
  transition: 0.5s;
}

ul li:hover {
  background: #33a3ee;
  transform: translateX(-10px);
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
  top: 0;
  left: -40px;
  width: 40px;
  height: 100%;
  background: #eeeeff;
  transform-origin: right;
  transform: skewY(45deg);
  transition: 0.5s;
}

ul li::after {
  content: '';
  position: absolute;
  top: -40px;
  left: 0px;
  width: 100%;
  height: 40px;
  background: #eeeeff;
  transform-origin: bottom;
  transform: skewX(45deg);
  transition: 0.5s;
}

ul li a {
  text-decoration: none;
  color: #999;
  display: block;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  transition: 0.5s;
}

ul li:hover a {
  color: #fff;
}

ul li:last-child::after {
  box-shadow: -120px 120px 20px rgba(0, 0, 0, 0.25);
}
</style>
