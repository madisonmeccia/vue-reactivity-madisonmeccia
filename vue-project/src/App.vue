<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
</script>

<template>
  <header>
    <h1 class="h">build your dream acai bowl order!</h1>
    <img
      alt="bowl"
      class="bowl"
      src="./assets/bowl.png"
      width="325"
      height="325"
    />
  </header>

  <main>
    <TheWelcome />
  </main>
</template>
<style scoped>
.bowl {
  margin-left: 110px;
  z-index: 1;
  margin-bottom: 10px;
}
.h {
  position: absolute;
  margin-left: 150px;
  margin-top: 110px;
  z-index: 2;
  font-family: fantasy;
  font-weight: bold;
  color: white;
  text-align: center;
  width: 250px;
}
</style>
