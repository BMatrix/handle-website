<template>
  <div :class="['text', reverse ? 'reversetitleoverlined' : '']">
    <div class="box"></div>
    <slot></slot>
  </div>
</template>

<style scoped>
.text {
  display: flex;
  flex-direction: column;
}
.text * {
  padding: 0;
  margin-bottom: 0.7em;
  font-family: HelveticaNeueBold;
}
.box {
  display: block;
  width: 1.5em;
  height: 0.5em;
  background-color: #e35d5b;
  margin: 0;
}
.reversetitleoverlined {
  align-items: flex-end;
}
</style>

<script>
export default {
  props: {
    reverse: {
      type: Boolean,
      default: false
    }
  }
};
</script>