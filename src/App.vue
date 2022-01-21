<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <hr />
  <div class="color">子模块</div>
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <ccc></ccc>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.color {
  color: blue;
  font-size: 26px;
  font-weight: 700;
}
</style>
