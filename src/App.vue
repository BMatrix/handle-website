<template>
  <div>
    <v-app>
      <!-- <Toolbar></Toolbar> -->
      <transition name="fade" mode="out-in">
        <router-view></router-view>
      </transition>
      <Footer></Footer>
    </v-app>
  </div>
</template>

<script>
import Toolbar from "./components/Toolbar.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Toolbar,
    Footer
  }
};
</script>

<style scoped>
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
