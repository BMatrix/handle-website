<template>
  <v-toolbar flat>
    <v-toolbar-items id="main">
      <router-link class="logo" :to="{ name: 'Home'}">
        <img src="logo.png" />
      </router-link>
      <div id="links">
        <router-link class="link" :to="{ name: 'Home'}">
          <div>
            <p>HOME</p>
          </div>
        </router-link>
        <router-link class="link" :to="{ name: 'About'}">
          <div>
            <p>ABOUT</p>
          </div>
        </router-link>
        <router-link class="link" :to="{ name: 'Team'}">
          <div>
            <p>TEAM</p>
          </div>
        </router-link>
      </div>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  name: "Toolbar",
  data() {
    return {
      a: 0
    };
  }
};
</script>

<style scoped>
#main {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

.logo {
  height: inherit;
}
.logo img {
  height: inherit;
  width: auto;
  padding: 2%;
  transition: all 0.3s ease-in-out;
}
.logo img:hover {
  padding: 1.5%;
  transition: all 0.3s ease-in-out;
}

#links {
  display: flex;
  align-self: center;
  align-items: center;
  height: inherit;
}
.link {
  transition: all 0.3s ease-in-out;
  height: inherit;
  padding: 0 20px 0 20px;
  color: black;
  font-family: Arial;
  font-size: 1.5em;
}
.link:hover {
  transition: all 0.3s ease-in-out;
  background-color: #f61f28;
  color: white;
}
.link div {
  height: inherit;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
p {
  height: 1em;
}
</style>