<template>
  <div id="app">
    <Header />
    <main class="container"><Albums /></main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Albums from "./components/Albums.vue";

export default {
  name: "App",
  components: {
    Header,
    Albums,
  },
};
</script>

<style lang="scss">
@import "./scss/style.scss";
</style>
