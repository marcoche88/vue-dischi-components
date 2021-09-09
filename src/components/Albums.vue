<template>
  <section id="album-container">
    <Card v-for="(disc, index) in discs" :key="index" :disc="disc" />
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