<template>
  <header>
    <div class="container">
      <section class="menu-container">
        <img src="../assets/logo.png" alt="logo" />
        <div class="select-genre">
          <select name="genre">
            <option value="all">Tutti</option>
          </select>
        </div>
      </section>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
header {
  background-color: #2e3a46;
  height: 70px;
  padding: 10px 20px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  .menu-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    img {
      height: 50px;
    }
  }
}

select {
  width: 200px;
  height: 30px;
  background-color: #7c8fa1;
}
</style>