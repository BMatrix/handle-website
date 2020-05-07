<template>
  <div class="footer">
    <p class="cr">Copyright Handle 2019-2020</p>
    <div class="contact">
      <a href="https://www.instagram.com/handleantwerp/" target="_blank">
        <v-icon class="icon">mdi-instagram</v-icon>
      </a>
      <router-link :to="'Contact'">
        <v-icon class="icon">mdi-forum-outline</v-icon>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped>
.footer {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 0.5em 2em 0.5em 2em;
  background-color: #757575;
}

.cr {
  color: blue;
  font-size: 1.2em;
  margin: 0px;
  padding: 0px;
}

.contact {
  margin-right: 1%;
  display: flex;
  flex-direction: row;
  gap: 1.5em;
}
.icon {
  background-color: lightgray;
  color: black;
  border-radius: 50%;
  padding: 25%;
}
</style>
