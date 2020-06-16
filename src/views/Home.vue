<template>
  <div class="home">
    <Header :backgroundimage="'images/headers/Explore.png'" :activepage="0" :buttonlink="'About'">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
      <template v-slot:button>{{ text.buttontext }}</template>
    </Header>
    <div class="galerysection">
      <Galery
        class="galery"
        :image11="'images/models/slim_old4.png'"
        :image21="'images/models/slim_software2.png'"
        :image31="'images/models/slim1.png'"
        :image12="'images/models/big1.png'"
        :image22="'images/models/big2.png'"
        :image32="'images/models/big_multi2.png'"
        :image13="'images/ui/intro.png'"
        :image23="'images/ui/fooddrink.png'"
        :image33="'images/ui/healthcare.png'"
      ></Galery>
      <div>
        <TitleOverlined :reverse="true">
          <h2>{{ text.header1 }}</h2>
        </TitleOverlined>
        <p v-for="text in text.paragraph1" :key="text">{{ text }}</p>
      </div>
    </div>
    <div class="animation">
      <video src="videos/animation.mp4" controls></video>
    </div>
    <div class="other">
      <DescribedImage
        class="describedimage"
        :image="'images/enviroments/enviroment1.png'"
        :reverse="true"
      >
        <template v-slot:title>{{ text.header2 }}</template>
        <template v-slot:text>
          <p v-for="text in text.paragraph2" :key="text">{{ text }}</p>
        </template>
      </DescribedImage>
      <DescribedImage
        class="describedimage"
        :image="'images/models/multi.png'"
      >
        <template v-slot:title>{{ text.header3 }}</template>
        <template v-slot:text>
          <p v-for="text in text.paragraph3" :key="text">{{ text }}</p>
        </template>
      </DescribedImage>
    </div>
    <Interested class="interested"></Interested>
  </div>
</template>

<style scoped>
h2 {
  font-size: 2em;
  padding: 0.5em 0 0.5em 0.3em;
}

.animation {
  background-color: #121726;
  color: white;
  text-align: center;
  padding: 5em 0 5em 0;
}
.animation video {
  min-width: 30em;
  max-width: 50%;
}

.other .describedimage {
  margin: 5em auto 5em auto;
  width: 80%;
}

.galerysection {
  margin: 5em auto 5em auto;
  width: 80%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.galerysection .galery {
  margin: 2em 2% 2em 0;
  width: 60%;
  flex-shrink: 0;
}
.galerysection div {
  text-align: right;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>

<script>
import { Home } from "../lang/en.js";
import Header from "../components/Header.vue";
import Galery from "../components/Galery.vue";
import DescribedImage from "../components/DescribedImage.vue";
import TitleOverlined from "../components/TitleOverlined.vue";
import Interested from "../components/Interested.vue";
export default {
  components: {
    Header,
    Galery,
    DescribedImage,
    TitleOverlined,
    Interested
  },
  data() {
    return {
      text: new Home()
    };
  }
};
</script>