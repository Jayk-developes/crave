<script setup lang="ts">
const navbarList = ["1", "2", "3", "4", "5"];
</script>

<template>
  <div class="topNav">
    <div>Following</div>
    <div>Discover</div>
  </div>
  <div class="navbar">
    <ul>
      <li v-for="listItem in navbarList">{{ listItem }}</li>
    </ul>
  </div>
  <div class="navCircle"></div>
</template>

<style scoped>

.navbar {
  z-index: 20;
  position: fixed;
  justify-content: space-between;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: #aaa;

  ul {
    padding: 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    text-align: center;

    li {
      height: 1rem;
      text-align: center;
      list-style: none;
    }

    li:nth-child(3) {
      padding-bottom: 1.5rem;
      font-size: 1.5rem;

    }
  }
}

.navCircle {
  position: fixed;
  width: 6rem;
  height: 6rem;
  z-index: 10;
  border-radius: 50%;

  bottom: 0;
  left: 50%;
  transform: translate(-50%, 0);
  background-color: #aaa;
}

.topNav {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-top: 1rem;
  font-size: 1.5em;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;

}
</style>