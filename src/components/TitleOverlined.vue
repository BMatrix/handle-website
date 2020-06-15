<template>
  <div class="core">
    <div :class="reverse ? 'reversetitleoverlined' : ''">
      <div class="box"></div>
    </div>
    <slot></slot>
  </div>
</template>

<style scoped>
.core div {
  margin: 0;
  display: flex;
}
.core .reversetitleoverlined{
  justify-content: flex-end;
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