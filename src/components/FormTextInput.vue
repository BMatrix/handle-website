<template>
  <div>
    <input class="test" :type="type" :placeholder="placeholder" :required="required" />
  </div>
</template>

<script>
export default {
  props: {
    type: String,
    placeholder: String,
    required: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style>
.test {
  font-family: HelveticaNeueBold;
  padding: 1%;
  padding-left: 1.3%;
  margin: 8px 0 8px 0;
  border: 2px solid #e35d5b;
  flex-grow: 1;
  border-radius: 999em;
}
</style>