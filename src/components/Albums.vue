<template>
  <section id="album-container">
    <Card />
  </section>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Albums",
  components: {
    Card,
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