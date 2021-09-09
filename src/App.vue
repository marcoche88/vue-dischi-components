<template>
  <div id="app">
    <Header @search="searchAlbums" />
    <main class="container"><Albums :genre="genre" /></main>
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
  data() {
    return {
      genre: "all",
    };
  },
  methods: {
    searchAlbums(genre) {
      this.genre = genre;
    },
  },
};
</script>

<style lang="scss">
@import "./scss/style.scss";
</style>
