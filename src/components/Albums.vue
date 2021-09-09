<template>
  <section id="album-container">
    <Card v-for="(disc, index) in filteredDiscs" :key="index" :disc="disc" />
  </section>
</template>

<script>
import axios from "axios";
import Card from "./Card.vue";

export default {
  name: "Albums",
  components: {
    Card,
  },
  data() {
    return {
      discs: [],
    };
  },
  props: ["genre"],
  computed: {
    sortedDiscs() {
      const sortedArr = [...this.discs];
      return sortedArr.sort((a, b) => {
        return a.year - b.year;
      });
    },
    filteredDiscs() {
      if (this.genre === "all") return this.sortedDiscs;
      return this.sortedDiscs.filter(
        (disc) => disc.genre.toLowerCase() === this.genre
      );
    },
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.discs = res.data.response;
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>

<style scoped lang="scss">
#album-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>