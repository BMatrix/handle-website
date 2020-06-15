<template>
  <div>
    <form class="form gap">
      <div>
        <input type="text" :placeholder="text.first_name" required />
        <input type="text" :placeholder="text.last_name" required />
        <input type="text" :placeholder="text.phone_number" required />
        <input type="email" :placeholder="text.email" required />
      </div>
      <div>
        <textarea rows="4" :placeholder="text.message" required />
      </div>
      <div>
        <input type="submit" :value="text.button" />
      </div>
    </form>
  </div>
</template>

<style scoped>
form {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: stretch;
  font-family: HelveticaNeueBold;
}
form div {
  display: flex;
  flex-direction: column;
}
form div * {
  padding: 2%;
  padding-left: 3%;
  margin: 8px 0 8px 0;
  border: 2px solid #e35d5b;
  border-radius: 0.5em;
  flex-grow: 1;
}

.gap {
  --gap: 3em;
  display: inline-flex;
  margin: calc(-1 * var(--gap)) 0 0 calc(-1 * var(--gap));
  width: calc(100% + var(--gap));
}
.gap > * {
  margin: var(--gap) 0 0 var(--gap);
}


form div:first-child {
  flex-basis: 20%;
}
form div:first-child * {
  border-radius: 999em;
  padding: 5%;
  padding-left: 5%;
}

form div:nth-child(2) {
  flex-grow: 1;
}

form div:last-child {
  flex-basis: 5%;
}
form div:last-child * {
  background-color: #e35d5b;
  color: white;
  writing-mode: sideways-lr;
}
</style>

<script>
import { Form } from "../lang/en.js";
export default {
  data() {
    return {
      text: new Form()
    };
  }
};
</script>