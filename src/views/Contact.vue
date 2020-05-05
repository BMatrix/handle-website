<template>
  <div class="contact">
    <Header :middle="false" :backgroundimage="'enviroments/enviroment1.jpg'" :backgroundcolor="'#'" :toolbarcolor="'#00000000'" :activepage="3">
      <template v-slot:title>Title</template>
      <template v-slot:text>Lorem ipsum dolor sit amet consectetur adipisicing elit. A mollitia ea nulla voluptate asperiores beatae consectetur excepturi aliquam quasi ipsa saepe tempora quas, ipsum officiis labore, debitis omnis sunt necessitatibus. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nisi quos nam nihil fugit unde, amet saepe reprehenderit reiciendis. Dolores dolorem, ut vero in soluta consectetur minima corporis non officiis fuga!</template>
    </Header>
  </div>
</template>

<style scoped>
.contact {
  height: 100%;
}
</style>

<script>
import Header from "../components/Header.vue";
export default {
  components: {
    Header
  }
};
</script>