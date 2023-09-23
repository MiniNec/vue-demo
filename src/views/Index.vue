<script setup lang="ts"></script>

<template>
  <div
    style="
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    "
  >
    <ul>
      <li><a>桃花源</a></li>
      <li><a>参仙院</a></li>
      <li><a>菊花台</a></li>
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
  transform: skewY(-60deg);
}

ul li {
  position: relative;
  list-style: none;
  width: 100px;
  background: #eeeeee;
  padding: 15px;
  font-size: 25px;
}

ul li a {
  text-decoration: none;
  color: #999;
  display: block;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  transition: 0.5s;
  font-weight: 1000;
}

ul li:hover a {
  color: #fff;
}

ul li::before {
  content: '';
  position: absolute;
  top: 0;
  left: -40px;
  width: 40px;
  height: 100%;
  background: #d00;
  transform-origin: right;
  transform: skewY(45deg);
}
</style>
