<template>
  <div class="contact">
    <Header :backgroundimage="'images/headers/Cancel.jpg'" :middle="true" :activepage="3">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
      <template v-slot:subtitle>{{ text.subtitle }}</template>
    </Header>
    <Tabs class="form">
      <div>
        <p>Cancel Tickets</p>
        <p>Change Reservation</p>
        <p>Cancel Reservation</p>
      </div>
      <div>
        <p>Content1</p>
        <p>Content2</p>
        <div>
          <h2>Fill in your order number</h2>
          <FormTextInput :type="text" :placeholder="'Order number #'" :required="true"></FormTextInput>
          <h2>Fill in your peronal information</h2>
          <DefaultForm></DefaultForm>
        </div>
      </div>
    </Tabs>
  </div>
</template>

<style scoped>
h2 {
  margin-top: 2em;
  font-family: HelveticaNeueBold;
  font-size: 2em;
}

.form {
  margin: 4em auto 4em auto;
  padding: 2em;
  width: 85%;
}
</style>

<script>
import { Cancel } from "../lang/en.js";
import Header from "../components/Header.vue";
import Tabs from "../components/Tabs.vue";
import DefaultForm from "../components/DefaultForm.vue";
import FormTextInput from "../components/FormTextInput.vue";
export default {
  components: {
    Header,
    Tabs,
    DefaultForm,
    FormTextInput
  },
  data() {
    return {
      text: new Cancel()
    };
  }
};
</script>