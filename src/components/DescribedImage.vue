<template>
  <div :class="['content', 'gap', reverse ? 'reverse' : '']">
    <div class="text">
      <TitleOverlined :reverse="reverse">
        <h2>
          <slot name="title"></slot>
        </h2>
      </TitleOverlined>
      <slot name="text"></slot>
    </div>
    <!--<img :src="imageleft" v-if="imageleft != null" />-->
    <img :src="image" />
  </div>
</template>

<style scoped>
.gap {
  --gap: 15%;
}

.content {
  width: 80%;
  display: flex;
  flex-direction: row;
}
img {
  object-fit: cover;
  width: 50%;
  margin-left: calc(var(--gap) / 2);
  border-radius: 4px;
}
img:first-child {
  flex-grow: 1;
}
/*img:nth-child(2) {
  position: absolute;
  height: fit-content;
  left: 0;
  transform: translateX(-90%);
}*/

.text {
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  margin-right: calc(var(--gap) / 2);
}
.text p {
  font-family: helveticaNeueLight;
  width: 100%;
  margin-top: 0;
}
.text h2 {
  font-size: 2em;
  font-family: HelveticaNeueBold;
  padding-bottom: 1.5em;
  margin-right: 0;
}
.text * {
  width: 100%;
}

.reverse {
  flex-direction: row-reverse;
}
.reverse .text {
  align-items: flex-end;
  text-align: right;
  margin-right: 0;
  margin-left: calc(var(--gap) / 2);
}
.reverse img {
  margin-right: calc(var(--gap) / 2);
  margin-left: 0;
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