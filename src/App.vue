<template>
  <div id="app">
    <router-view />
    <About />
  </div>
</template>

<style></style>

<script>
import About from "./views/About.vue";
export default {
  components: {
    About,
  },
};
</script>
