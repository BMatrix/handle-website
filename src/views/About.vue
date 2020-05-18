<template>
  <div class="about">
    <Header :backgroundimage="'models/model3.png'" :activepage="1">
      <template v-slot:title>{{ text.title }}</template>
      <template v-slot:text>{{ text.description }}</template>
    </Header>
    <div class="information">
      <DescribedImage class="work" :image="'enviroments/enviroment1.jpg'" :reverse="true">
        <template v-slot:title>{{ text.header1 }}</template>
        <template v-slot:text>{{ text.paragraph1 }}</template>
      </DescribedImage>
      <DescribedImage class="work" :image="'enviroments/enviroment2.jpg'">
        <template v-slot:title>{{ text.header2 }}</template>
        <template v-slot:text>{{ text.paragraph2 }}</template>
      </DescribedImage>
    </div>
    <div class="product">
      <div>
        <h2>{{ text.header3 }}</h2>
        <p>{{ text.paragraph3 }}</p>
        <Galery
          :nonav="true"
          :image11="'models/model1.png'"
          :image21="'enviroments/enviroment1.jpg'"
          :image31="'posters/poster1.jpg'"
        ></Galery>
      </div>
    </div>
    <Interested class="interested"></Interested>
  </div>
</template>

<style scoped>
.about {
  height: 100%;
}

.information * {
  margin: 4em 0 4em 0;
}

.product {
  padding: 4em 0 5em 0;
  background-color: grey;
}
.product > div {
  margin-right: auto;
  margin-left: auto;
  width: 90%;
}
.product div h2 {
  color: blue;
  font-size: 3em;
}
.product div p {
  margin: 3em 0 4em 0;
}

.about .interested {
  margin: 8em 0 8em 0;
}
</style>

<script>
import { About } from "../lang/en.js";
import Header from "../components/Header.vue";
import DescribedImage from "../components/DescribedImage.vue";
import Galery from "../components/Galery.vue";
import Interested from "../components/Interested.vue";
export default {
  components: {
    Header,
    DescribedImage,
    Galery,
    Interested
  },
  data() {
    return {
      text: new About()
    };
  }
};
</script>