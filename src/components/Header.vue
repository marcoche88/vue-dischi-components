<template>
  <header>
    <div class="container">
      <section class="menu-container">
        <img src="../assets/logo.png" alt="logo" />
        <div class="select-genre">
          <select
            name="genre"
            v-model="selectGenre"
            @change="$emit('search', selectGenre)"
          >
            <option value="all">Tutti</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
          </select>
          <select
            name="author"
            v-model="selectAuthor"
            @change="$emit('searchAuthor', selectAuthor)"
          >
            <option value="all">Tutti</option>
            <option value="deep purple">Deep Purple</option>
            <option value="michael jacjson">Michael Jacjson</option>
            <option value="bon jovi">Bon Jovi</option>
            <option value="metallica">Metallica</option>
            <option value="queen">Queen</option>
            <option value="sting">Sting</option>
            <option value="dave weckl">Dave Weckl</option>
            <option value="iron maiden">Iron Maiden</option>
            <option value="eric clapton">Eric Clapton</option>
            <option value="steve gadd band">Steve Gadd Band</option>
          </select>
        </div>
      </section>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      selectGenre: "all",
      selectAuthor: "all",
    };
  },
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
  margin: 0 10px;
  background-color: #7c8fa1;
}
</style>