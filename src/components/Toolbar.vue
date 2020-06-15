<template>
  <div>
    <div id="bar">
      <router-link class="logo" :to="{ name: 'Home'}">
        <img src="images/logo/Icon.png" />
        <img v-if="clap" class="clap" src="images/logo/Icon.png" />
        <div class="clapbox" v-on:click="enableClap"></div>
        <img src="images/logo/Text.png" />
      </router-link>
      <router-link
        v-for="link in links"
        :key="link.id"
        :class="['link', isChrome ? link.id == activeid ? 'active' : '' : link.id == activeid ? ['active', 'activebar'] : 'hover']"
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
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 6em;
}
.logo img:first-child {
  height: 6em;
  margin-right: 1.5em;
}
.logo img:last-child {
  height: 1.5em;
}
.logo .clap {
  transform: translateX(-500%);
  transition: all 0.7s ease-in-out;

  height: 5.6em;
  position: absolute;
}
.logo:hover .clap {
  transform: translateX(-2%);
  transition: all 0.3s ease-in;
}
.clapbox{
  position: absolute;
  width: 0.8em;
  height: 0.8em;
  transform: translateY(-120%);
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
.hover:hover {
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
.activebar::after {
  content: "";
  display: block;
  background-color: #e35d5b;
  height: 0.2em;
  width: 50%;
  transform: translateX(50%);
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
      isChrome: false,
      clap: false,
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
          name: text.navigation_cancel,
          link: "Cancel"
        },
        {
          id: 4,
          name: text.navigation_contact,
          link: "Contact"
        }
      ]
    };
  },
  created: function() {
    var isChromium = window.chrome;
    var winNav = window.navigator;
    var vendorName = winNav.vendor;
    var isOpera = typeof window.opr !== "undefined";
    var isIEedge = winNav.userAgent.indexOf("Edge") > -1;
    var isIOSChrome = winNav.userAgent.match("CriOS");

    if (isIOSChrome) {
      // is Google Chrome on IOS
    } else if (
      isChromium !== null &&
      typeof isChromium !== "undefined" &&
      vendorName === "Google Inc." &&
      isOpera === false &&
      isIEedge === false
    ) {
      // is Google Chrome
      this.isChrome = true;
    } else {
      // not Google Chrome
    }
  },
  methods: {
    enableClap: function(){
      this.clap = true;
    }
  }
};
</script>