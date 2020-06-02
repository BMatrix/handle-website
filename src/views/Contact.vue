<template>
  <div class="contact">
    <Header :backgroundimage="'images/headers/Contact.jpg'" :middle="true" :activepage="4">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
    </Header>
    <div class="form">
      <h2>Contact Form</h2>
      <DefaultForm></DefaultForm>
    </div>
  </div>
</template>

<style scoped>
.form {
  margin: 4em auto 4em auto;
  padding: 2em;
  width: 85%;
}
h2{
  font-family: HelveticaNeueBold;
  font-size: 2em;
}
.form *:last-child {
  margin-top: 2em;
}
</style>

<script>
import { Contact as text } from "../lang/en.js";
import Header from "../components/Header.vue";
import DefaultForm from "../components/DefaultForm.vue";
export default {
  components: {
    Header,
    DefaultForm
  },
  data() {
    return {
      text: new text()
    };
  }
};
</script>