<template>
  <div class="member">
    <v-avatar size="170px" :class="['avatar']">
      <img :src="image" />
      <div :class="['grayscale', redscale ? 'redscale' : '']"></div>
    </v-avatar>
    <div class="text">
      <h2>
        <slot name="name"></slot>
      </h2>
      <h3>
        <slot name="role"></slot>
      </h3>
      <p>
        <slot name="quote"></slot>
      </p>
    </div>
  </div>
</template>

<style scoped>
.member {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0;
}

.grayscale {
  position: absolute;
  width: inherit;
  height: inherit;
  transition: all 0.3s ease-in-out;
  /*background-color: #777777a2;*/
}
/*.grayscale:hover {
  transition: all 0.3s ease-in-out;
  background-color: #00000000;
}*/
.redscale {
  background-color: #e35d5bb6;
}

.text {
  margin-left: 2em;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: auto;
}
.text h2 {
  font-family: HelveticaNeueBold;
}
.text h3 {
  font-family: HelveticaNeueLight;
}
</style>

<script>
export default {
  name: "Member",
  props: {
    image: String,
    redscale: {
      type: Boolean,
      default: false
    }
  }
};
</script>