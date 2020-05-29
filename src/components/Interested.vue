<template>
  <div class="interested">
    <h2>{{ text.title }}</h2>
    <router-link class="link" :to="'Contact'">
      <h3 class="button">{{ text.button }}</h3>
    </router-link>
  </div>
</template>

<style scoped>
.interested {
  display: block;
  text-align: center;
  background-color: #121726;
  padding: 4em 0 4em 0;
}
h2 {
  color: white;
  /*font-size: 2em;*/
}
.link {
  display: inline-block;
  margin-top: 2em;
}
.button {
  display: inline-block;
  padding: 0.3em 1em 0.3em 1em;
  border-radius: 999em;
  background-color: #e35d5b;
  color: white;
}
</style>

<script>
import { Interested } from "../lang/en.js";
export default {
  data(){
    return {
      text: new Interested()
    }
  }
}
</script>