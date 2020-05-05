<template>
  <div class="home">
    <Header :backgroundimage="'enviroments/enviroment1.jpg'" :activepage="0">
      <template v-slot:title>You Can Hande it!</template>
    </Header>
    <div class="main">
      <div class="center">
        <div class="content">
          <img src="models/model1.png" />
          <div>
            <h2>Title Here</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem necessitatibus voluptas fugit quaerat nemo quos, aut at eum voluptatum, reiciendis, eos illum dolor corrupti quasi odio architecto adipisci maxime fugiat.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.center {
  margin-left: auto;
  margin-right: auto;
  width: 70%;
  text-align: center;
}

.main {
  width: 100%;
  height: auto;
  background-color: white;
}

.content {
  padding: 2em 0 2em 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.content img {
  width: 40%;
  flex-shrink: 0;
}
.content div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: left;
  padding-left: 10%;
}
</style>

<script>
import Header from "../components/Header.vue";
export default {
  components: {
    Header
  }
};
</script>