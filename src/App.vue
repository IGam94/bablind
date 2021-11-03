<template>
  <div id="app">
    <About />
  </div>
</template>

<style></style>

<script>
import About from "./views/About.vue";
import Maps from "./views/maps.vue";
import "./assets/css/style.css";
export default {
  components: {
    About,
    Maps,
  },
};
</script>
