<template>
  <div>
    <Toolbar></Toolbar>
    <v-app>
      <router-view></router-view>
    </v-app>
  </div>
</template>

<script>
import Toolbar from "./components/Toolbar.vue";
export default {
  name: "App",
  components: {
    Toolbar
  }
};
</script>

<style scoped>

</style>
