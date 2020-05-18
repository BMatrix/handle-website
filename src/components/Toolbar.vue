<template>
  <v-toolbar flat :color="color">
    <v-toolbar-items id="main">
      <router-link class="logo" :to="{ name: 'Home'}">
        <img src="logo.png" />
      </router-link>
      <div id="links">
        <router-link
          v-for="link in links"
          :key="link.id"
          :class="['link', link.id == activeid ? 'active' : '']"
          :to="{ name: link.link}"
        >
          <div>
            <p>{{ link.name }}</p>
          </div>
        </router-link>
      </div>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
import { Navigation } from "../lang/en.js";
let text = new Navigation();
export default {
  name: "Toolbar",
  props: {
    color: {
      type: String,
      default: '#00000000'
    },
    activeid: Number
  },
  data() {
    return {
      links: [
        {
          id: 0,
          name: text.navigation_home,
          link: "Home"
        },
        {
          id: 1,
          name: text.navigation_about,
          link: "About"
        },
        {
          id: 2,
          name: text.navigation_contact,
          link: "Contact"
        }
      ]
    };
  }
};
</script>

<style scoped>
#main {
  width: 100%;
  display: flex;
  justify-content: space-between;
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
  text-decoration: none;
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

.active {
  text-decoration: underline;
  color: blue;
}
</style>