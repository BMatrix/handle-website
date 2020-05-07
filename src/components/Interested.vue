<template>
  <div class="interested">
    <h2>Are you interested?</h2>
    <h3>Feel free to contact us</h3>
    <router-link class="link" :to="'Contact'">
      <h3 class="button">Contact us</h3>
    </router-link>
  </div>
</template>

<style scoped>
.interested {
  display: block;
  text-align: center;
}
h2 {
  color: blue;
  font-size: 3em;
}
h3 {
  color: blue;
  font-size: 1.5em;
}
.link {
  display: inline-block;
  margin: 2em 0px 2em 0px;
}
.button {
  display: inline-block;
  padding: 0.2em 0.5em 0.2em 0.5em;
  border: solid blue 3px;
  border-radius: 15px;
}
</style>