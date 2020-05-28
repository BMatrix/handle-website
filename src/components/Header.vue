<template>
  <div class="header" :style="[image, color]">
    <Toolbar :activeid="activepage"></Toolbar>
    <div class="center">
      <div :class="[middle ? 'hidden' : 'text']">
        <h1>
          <slot name="title"></slot>
        </h1>
        <p>
          <slot name="text"></slot>
        </p>
      </div>
      <div :class="[middle ? 'middletext' : 'hidden']">
        <h1>
          <slot name="title"></slot>
        </h1>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  position: relative;
  height: 35em;
  width: 100%;
  background-position: center bottom;
  background-size: cover;
}
.center {
  width: 80%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.text h1 {
  color: blue;
  font-size: 3em;
  margin-bottom: 0.5em;
}
.text p {
  width: 60%;
}

.middletext {
  margin-left: auto;
  margin-right: auto;
  width: 90%;
}
.middletext h1 {
  color: black;
  font-size: 2.5em;
}

.hidden {
  display: none;
}
</style>

<script>
import Toolbar from "../components/Toolbar.vue";
export default {
  name: "Header",
  components: {
    Toolbar
  },
  props: {
    middle: {
      type: Boolean,
      default: false
    },
    backgroundimage: {
      type: String,
      default: null
    },
    backgroundcolor: {
      type: String,
      default: null
    },
    activepage: Number
  },
  data() {
    let image = {};
    let color = {};
    if (this.backgroundimage != null) {
      image = {
        "background-image": `url(${this.backgroundimage})`
      };
    }
    if (this.backgroundcolor != null) {
      color = {
        "background-color": this.backgroundcolor
      };
    }
    return {
      image: image,
      color: color
    };
  }
};
</script>