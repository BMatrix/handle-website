<template>
  <div :class="['member', reverse ? 'reverse' : '']">
    <v-avatar size="200px" :class="['avatar']">
      <img :src="image" />
      <div :class="['grayscale', redscale ? 'redscale' : '']"></div>
    </v-avatar>
    <div id="text" :class="[reverse ? 'righttext' : 'lefttext']">
      <h2>
        <slot name="name"></slot>
      </h2>
      <h3>
        <slot name="role"></slot>
      </h3>
      <p>
        <slot name="description"></slot>
      </p>
    </div>
  </div>
</template>

<style scoped>
.member {
  display: flex;
  flex-direction: row;
}
.reverse {
  flex-direction: row-reverse;
}

.grayscale {
  position: absolute;
  width: inherit;
  height: inherit;
  transition: all 0.3s ease-in-out;
  background-color: #777777a2;
}
.grayscale:hover {
  transition: all 0.3s ease-in-out;
  background-color: #00000000;
}
.redscale {
    background-color: #f73b3ba2;
}

#text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 50%;
}
.lefttext {
  text-align: left;
  margin-left: 5%;
}
.righttext {
  text-align: right;
  margin-right: 5%;
}
</style>

<script>
export default {
  name: "Member",
  props: {
    image: String,
    reverse: {
      type: Boolean,
      default: false
    },
    redscale: {
        type: Boolean,
        default: false
    }
  }
};
</script>