<template>
  <div id="app">
    <Header @search="searchAlbums" @searchAuthor="searchAuthor" />
    <main class="container"><Albums :genre="genre" :author="author" /></main>
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
      author: "all",
    };
  },
  methods: {
    searchAlbums(genre) {
      this.genre = genre;
    },
    searchAuthor(author) {
      this.author = author;
    },
  },
};
</script>

<style lang="scss">
@import "./scss/style.scss";
</style>
