<template>
  <div class="header">
    <img class="image" :src="backgroundimage" alt />
    <Toolbar :activeid="activepage"></Toolbar>
    <div class="center">
      <div class="text">
        <h1>
          <slot name="title"></slot>
        </h1>
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
  height: 35em;
  width: 100%;
  background-position: center bottom;
  background-size: cover;
}
.center {
  width: 80%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.text h1 {
  margin-bottom: 0.7em;
  font-family: HelveticaNeueBold;
}
.text h1::before {
  content: "";
  display: block;
  border-bottom: solid #e35d5b 0.2em;
  width: 1em;
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
.image {
  position: absolute;
  height: 100%;
  right: 0;
  top: 0;
  clip-path: polygon(60% 0, 100% 0, 65% 100%, 25% 100%);
  transform: translateX(10%);
}
</style>

<script>
import Toolbar from "../components/Toolbar.vue";
export default {
  name: "Header",
  components: {
    Toolbar
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
  }
};
</script>