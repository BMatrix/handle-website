<template>
  <div>
    <v-app>
      <transition name="fade" mode="out-in">
        <router-view></router-view>
      </transition>
      <Footer></Footer>
    </v-app>
  </div>
</template>

<script>
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Footer
  }
};
</script>

<style scoped>
div{
  background-color: #EEEEEF;
}
.closer {
  width: 100%;
  height: 3em;
  background-color: #757575;
}

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>

<style>
@font-face {
  font-family: HelveticaNeueLight;
  src: url("../public/fonts/HelveticaNeueLight.ttf");
}
@font-face {
  font-family: HelveticaNeueBold;
  src: url("../public/fonts/HelveticaNeueBold.ttf");
}
</style>
