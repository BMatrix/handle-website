<template>
  <div>
    <div id="bar">
      <router-link class="logo" :to="{ name: 'Home'}">
        <img src="images/logo/Icon.png" />
      </router-link>
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
  </div>
</template>

<style scoped>
#bar {
  margin-left: auto;
  margin-right: auto;
  width: 80%;
  transform: translateY(3em);
  height: 4em;
  display: flex;
  justify-content: space-around;
  background-color: white;
  border-radius: 999em;
  align-items: center;
  box-shadow: 0px 0.2em 0.2em 0.1em #b4b4b47e;
}

.logo {
  height: 2em;
}
.logo img {
  height: 2em;
}

.link {
  transition: all 0.3s ease-in-out;
  height: inherit;
  padding: 0 2% 0 2%;
  color: black;
  font-family: HelVeticaNeueLight;
  font-size: 1em;
  text-decoration: none;
}
.link:hover {
  transition: all 0.3s ease-in-out;
  background-color: #e35d5b;
  color: white;
}
.link div {
  position: relative;
  height: inherit;
  display: flex;
  align-items: center;
}
.link div p {
  height: 0.7em;
  padding-bottom: 0px;
}

.active {
  color: #e35d5b;
  font-family: HelveticaNeueBold;
}
.active::after {
  content: "";
  display: block;
  border-bottom: solid #e35d5b 0.2em;
}
</style>

<script>
import { Navigation } from "../lang/en.js";
let text = new Navigation();
export default {
  name: "Toolbar",
  props: {
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
          name: text.navigation_team,
          link: "Team"
        },
        {
          id: 3,
          name: text.navigation_contact,
          link: "Contact"
        }
      ]
    };
  }
};
</script>