<template>
  <div class="about">
    <Header :backgroundimage="'images/models/model3.png'" :activepage="1">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
    </Header>
    <div class="information">
      <DescribedImage :image="'images/enviroments/enviroment1.jpg'" :imageleft="'images/enviroments/enviroment1.jpg'">
        <template v-slot:title>{{ text.header1 }}</template>
        <template v-slot:text>{{ text.paragraph1 }}</template>
      </DescribedImage>
    </div>
    <Interested class="interested"></Interested>
  </div>
</template>

<style scoped>
.about {
  height: 100%;
}

.information * {
  margin: 4em auto 4em auto;
}
</style>

<script>
import { About } from "../lang/en.js";
import Header from "../components/Header.vue";
import DescribedImage from "../components/DescribedImage.vue";
import Interested from "../components/Interested.vue";
export default {
  components: {
    Header,
    DescribedImage,
    Interested
  },
  data() {
    return {
      text: new About()
    };
  }
};
</script>