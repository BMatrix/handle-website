<template>
  <div class="footer">
    <p class="cr">{{ text.footer_copyright }}</p>
  </div>
</template>

<script>
import { Footer } from "../lang/en.js";
export default {
  name: "Footer",
  data(){
    return {
      text: new Footer()
    }
  }
};
</script>

<style scoped>
.footer {
  position: relative;
  bottom: 0;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 1em 0 1em 0;
}

.cr {
  color: #888889;
  font-size: 1.2em;
  margin: 0px;
  padding: 0px;
}
</style>
