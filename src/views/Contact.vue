<template>
  <div class="contact">
    <Header :backgroundimage="'images/enviroments/enviroment1.jpg'" :middle="true" :activepage="2">
      <template v-slot:title>
      {{ text.title }}
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
import { Contact as text} from "../lang/en.js";
import Contact from "../components/Contact.vue";
import Header from "../components/Header.vue";
export default {
  components: {
    Header,
    Contact
  },
  data(){
    return {
      text: new text()
    }
  }
};
</script>