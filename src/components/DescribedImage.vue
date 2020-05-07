<template>
  <div :class="['content', reverse ? 'reverse' : '']">
    <div class="image">
      <img :src="image" />
    </div>
    <div class="text">
      <h2><slot name="title"></slot></h2>
      <p><slot name="text"></slot></p>
    </div>
  </div>
</template>

<style scoped>
.content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.content .image {
  box-flex: 1;
  flex: 1 1 auto;
  text-align: center;
  width: 55%;
  flex-shrink: 0;
}
.content .image img {
  border-radius: 20px;
  width: 100%;
}

.content .text {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.content .text * {
  margin-left: auto;
  margin-right: auto;
  width: 70%;
  text-align: justify;
}
.content .text h2 {
    text-align: center;
    font-size: 3em;
    color: blue;
    padding-bottom: 1em;
}

.reverse {
  flex-direction: row-reverse;
}
</style>

<script>
export default {
  name: "DescribedImage",
  props: {
    reverse: {
      type: Boolean,
      default: false
    },
    image: String
  }
};
</script>