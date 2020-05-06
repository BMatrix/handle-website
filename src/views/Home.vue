<template>
  <div class="home">
    <Header :backgroundimage="'enviroments/enviroment1.jpg'" :activepage="0">
      <template v-slot:title>You Can Hande it!</template>
    </Header>
    <div class="productidea">
      <h2>The Product Idea</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur sequi suscipit odit molestiae itaque cum! Dolore recusandae perspiciatis eaque, sequi, harum aspernatur doloribus ullam quae beatae numquam cum impedit deserunt! Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum iusto dolorum eaque placeat commodi a sapiente consectetur corporis voluptatem nam. Exercitationem ea officia commodi excepturi quaerat tempore tempora odio architecto. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti nam deserunt expedita quo dolor natus quidem placeat reprehenderit voluptatum atque eum, animi voluptatibus at ex iure odio illo voluptatem totam? Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto, dolorem autem expedita vel amet sint modi eum repellat accusamus in aliquid iure recusandae sed ea aperiam, nam eligendi! Blanditiis, ex? Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur laudantium quod deleniti debitis ducimus reiciendis obcaecati mollitia a, incidunt molestiae ullam voluptate itaque, sit officia eveniet iusto quae neque vel.</p>
      <Galery
        class="galery"
        :image11="'models/model1.png'"
        :image12="'models/model2.png'"
        :image13="'models/model3.png'"
        :image21="'enviroments/enviroment1.jpg'"
        :image22="'enviroments/enviroment2.jpg'"
        :image23="'enviroments/enviroment1.jpg'"
        :image31="'posters/poster1.jpg'"
        :image32="'posters/poster2.png'"
        :image33="'posters/poster3.png'"
      ></Galery>
    </div>
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
h2 {
  color: blue;
  font-size: 3em;
  margin: 1em 0 0.5em 0.3em;
}

.productidea {
  margin: 0 auto 0 auto;
  width: 80%;
}
.galery {
  margin: 2em 0 2em 0;
}

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
import Galery from "../components/Galery.vue";
export default {
  components: {
    Header,
    Galery
  }
};
</script>