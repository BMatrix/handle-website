<template>
  <div :class="['content', reverse ? 'reverse' : '']">
    <img :src="image" />
    <!--<img :src="imageleft" v-if="imageleft != null" />-->
    <div class="text">
      <TitleOverlined :reverse="true">
        <h2>
          <slot name="title"></slot>
        </h2>
      </TitleOverlined>
      <p>
        <slot name="text"></slot>
      </p>
    </div>
  </div>
</template>

<style scoped>
.content {
  width: 80%;
  display: flex;
  flex-direction: row;
  gap: 15%;
}
img {
  object-fit: cover;
  width: 50%;
}
img:first-child {
  flex-grow: 1;
}
img:nth-child(2) {
  position: absolute;
  height: fit-content;
  left: 0;
  transform: translateX(-90%);
}

.text {
  width: 50%;
}
.content .text p {
  font-family: helveticaNeueLight;
  text-align: right;
}
.content .text h2 {
  font-size: 2em;
  font-family: HelveticaNeueBold;
  padding-bottom: 1em;
  margin-right: 0;
}

.reverse {
  flex-direction: row-reverse;
}
</style>

<script>
import TitleOverlined from "./TitleOverlined";
export default {
  name: "DescribedImage",
  components: {
    TitleOverlined
  },
  props: {
    reverse: {
      type: Boolean,
      default: false
    },
    image: String,
    imageleft: {
      type: String,
      default: null
    }
  }
};
</script>