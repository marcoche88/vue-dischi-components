<template>
  <div class="card">
    <img src="" alt="" />
    <h2 class="title"></h2>
    <address class="author"></address>
    <time datetime="" class="year"></time>
  </div>
</template>

<script>
export default {
  name: "Card",
};
</script>

<style scoped lang="scss">
.card {
  background-color: #2e3a46;
  padding: 20px;
  margin: 20px;
  flex-basis: 190px;
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