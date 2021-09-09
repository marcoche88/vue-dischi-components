<template>
  <div class="card">
    <img :src="disc.poster" :alt="disc.title" />
    <h2 class="title">{{ disc.title }}</h2>
    <address class="author">{{ disc.author }}</address>
    <time :datetime="disc.year" class="year">{{ disc.year }}</time>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["disc"],
};
</script>

<style scoped lang="scss">
.card {
  background-color: #2e3a46;
  padding: 20px;
  margin: 20px;
  flex-basis: 200px;
  text-align: center;
  min-height: 350px;
  img {
    width: 100%;
    height: auto;
  }
  .title {
    color: #fff;
    margin: 15px 0;
    text-transform: uppercase;
    font-size: 22px;
  }
}

address,
time {
  color: #808080;
  font-size: 21px;
}

time {
  font-size: 16px;
}
</style>