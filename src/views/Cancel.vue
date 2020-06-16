<template>
  <div class="contact">
    <Header :backgroundimage="'images/headers/Cancel.png'" :middle="true" :activepage="3">
      <template v-slot:title>
        <h1>{{ text.title }}</h1>
      </template>
    </Header>
    <Tabs class="form">
      <div>
        <p>Cancel Tickets</p>
        <p>Change Reservation</p>
        <p>Cancel Reservation</p>
      </div>
      <div>
        <div class="border">
          <h2>{{ text.placeholder_cancel_tickets}}</h2>
        </div>
        <div class="border">
          <h2>{{ text.placeholder_change_reservation }}</h2>
        </div>
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

.border {
  border: solid 2px #e35d5b;
  border-radius: 999em;
  margin-top: 4em;
  padding: 1em 2em 1em 2em;
}
.border h2 {
  margin: 0;
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