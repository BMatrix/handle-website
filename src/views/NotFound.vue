<template>
  <div class="home">
    <Header :backgroundimage="'images/headers/Explore.jpg'">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
    </Header>
  </div>
</template>

<style scoped>
</style>

<script>
import { NotFound } from "../lang/en.js";
import Header from "../components/Header.vue";
export default {
  components: {
    Header
  },
  data() {
    return {
      text: new NotFound()
    };
  }
};
</script>