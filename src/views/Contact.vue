<template>
  <div class="contact">
    <Header :backgroundimage="'enviroments/enviroment1.jpg'" :middle="true" :activepage="3">
      <template v-slot:title>
        Have a question or want to collaborate with us?
        <br />Please get in touch.
      </template>
    </Header>
    <Contact class="form"></Contact>
  </div>
</template>

<style scoped>
.form {
  margin: 4em auto 4em auto;
  width: 85%;
}
</style>

<script>
import Contact from "../components/Contact.vue";
import Header from "../components/Header.vue";
export default {
  components: {
    Header,
    Contact
  }
};
</script>