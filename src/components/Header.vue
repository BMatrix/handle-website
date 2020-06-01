<template>
  <div class="header" :style="backgroundStyle">
    <!--<img class="image" :src="backgroundimage" alt />-->
    <Toolbar :activeid="activepage"></Toolbar>
    <div class="aligntext">
      <div class="text">
        <TitleOverlined>
          <slot name="title"></slot>
        </TitleOverlined>
        <p>
          <slot name="subtitle"></slot>
        </p>
        <router-link v-if="buttonlink != null" class="button" :to="{ name: buttonlink}">
          <p>
            <slot name="button"></slot>
          </p>
        </router-link>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  position: relative;
  height: 45em;
  width: 100%;
  background-position: left top;
  background-size: cover;
}
.aligntext {
  width: 80%;
  position: absolute;
  bottom: 10%;
  left: 50%;
  transform: translateX(-50%);
}
.text p {
  width: 60%;
  font-family: HelveticaNeueLight;
  font-size: 1.1em;
}
.button {
  text-decoration: none;
}
.button p {
  font-family: HelveticaNeueBold;
  width: fit-content;
  margin-top: 2em;
  padding: 0.3em 1em 0.3em 1em;
  border-radius: 999em;
  color: white;
  background-color: #e35d5b;
}
</style>

<script>
import Toolbar from "./Toolbar.vue";
import TitleOverlined from "./TitleOverlined.vue";
export default {
  name: "Header",
  components: {
    Toolbar,
    TitleOverlined
  },
  props: {
    middle: {
      type: Boolean,
      default: false
    },
    backgroundimage: {
      type: String,
      default: null
    },
    activepage: Number,
    buttonlink: {
      type: String,
      default: null
    }
  },
  data(){
    return {
      backgroundStyle: {
        'background-image': `url(${this.backgroundimage}`
      },
    }
  }
};
</script>