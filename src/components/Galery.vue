<template>
  <div class="galery">
    <div :class="['images', nonav ? 'nonav' : '']">
      <div :class="picked">
        <img :src="image11" />
        <img :src="image12" />
        <img :src="image13" />
      </div>
      <div :class="picked">
        <img :src="image21" />
        <img :src="image22" />
        <img :src="image23" />
      </div>
      <div :class="picked">
        <img :src="image31" />
        <img :src="image32" />
        <img :src="image33" />
      </div>
    </div>
    <div class="buttons" v-if="!nonav">
      <span v-on:click="select(1)">
        <span :class="radio1"></span>
      </span>
      <span v-on:click="select(2)">
        <span :class="radio2"></span>
      </span>
      <span v-on:click="select(3)">
        <span :class="radio3"></span>
      </span>
    </div>
  </div>
</template>

<style>
.galery{
  height: 300px;
}

.images {
  height: 90%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr;
  column-gap: 2%;
}
.nonav {
  height: 100%
}
.images div {
  display: grid;
  grid-template-rows: 1fr;
  overflow: hidden;
  background-color: #b3b3b3;
  border-radius: 1%;
}
.images div img {
  grid-area: 1 / 1 / 1 / 1;
  width: 100%;
  transform: translateX(0%);
  transition: all 0.3s ease-in-out;
  height: 100%;
  object-fit: cover;
}
.image1 :nth-child(1) {
  transform: translateX(0%);
}
.image1 :nth-child(2) {
  transform: translateX(100%);
}
.image1 :nth-child(3) {
  transform: translateX(200%);
}
.image2 :nth-child(1) {
  transform: translateX(-100%);
}
.image2 :nth-child(2) {
  transform: translateX(0%);
}
.image2 :nth-child(3) {
  transform: translateX(100%);
}
.image3 :nth-child(1) {
  transform: translateX(-200%);
}
.image3 :nth-child(2) {
  transform: translateX(-100%);
}
.image3 :nth-child(3) {
  transform: translateX(0%);
}

.buttons {
  height: 10%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding-top: 20px;
}
.buttons span {
  position: relative;
  display: block;
  content: "";
  width: 40px;
  height: 40px;
  background-color: transparent;
  border-radius: 50%;
  cursor: pointer;
}
.buttons span span {
  position: absolute;
  transform: translate(-50%, -50%);
  margin: 20px;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #e35d5b;
}
.buttons span span:before {
  position: relative;
  display: block;
  content: "";
  width: 6px;
  height: 6px;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background-color: white;
  border-radius: 50%;
}
.buttons span .selected:after {
  position: relative;
  display: block;
  content: "";
  width: 10px;
  height: 10px;
  bottom: 60%;
  background-color: #e35d5b;
  border-radius: 50%;
}
</style>

<script>
export default {
  name: "Galery",
  props: {
    nonav: {
      type: Boolean,
      default: false
    },
    image11: String,
    image12: String,
    image13: String,
    image21: String,
    image22: String,
    image23: String,
    image31: String,
    image32: String,
    image33: String
  },
  data() {
    return {
      picked: "image1",
      radio1: "selected",
      radio2: "",
      radio3: ""
    };
  },
  methods: {
    select(i) {
      if (i == 1) {
        this.radio1 = "selected";
        this.picked = "image1";
      } else {
        this.radio1 = "";
      }
      if (i == 2) {
        this.radio2 = "selected";
        this.picked = "image2";
      } else {
        this.radio2 = "";
      }
      if (i == 3) {
        this.radio3 = "selected";
        this.picked = "image3";
      } else {
        this.radio3 = "";
      }
    }
  }
};
</script>