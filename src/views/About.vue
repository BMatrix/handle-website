<template>
  <div class="about">
    <Header :backgroundimage="'images/headers/About.png'" :activepage="1">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
    </Header>
    <div class="information">
      <DescribedImage
        :image="'images/enviroments/enviroment2-2.png'"
        :reverse="true"
      >
        <template v-slot:title>{{ text.header1 }}</template>
        <template v-slot:text>
          <p>{{ text.paragraph1 }}</p>
        </template>
      </DescribedImage>
      <DescribedImage
        :image="'images/enviroments/enviroment3.png'"
      >
        <template v-slot:title>{{ text.header2 }}</template>
        <template v-slot:text>
          <p>{{ text.paragraph2 }}</p>
        </template>
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
  width: 80%;
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