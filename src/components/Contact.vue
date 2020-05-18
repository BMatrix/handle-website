<template>
  <div class="content">
    <h2>{{ text.title }}</h2>
    <form>
      <div>
        <input type="text"  :placeholder="text.first_name" required />
        <input type="text"  :placeholder="text.last_name" required />
        <input type="email" :placeholder="text.email" required />
        <input type="text"  :placeholder="text.company" />
        <textarea rows="4"  :placeholder="text.message" required />
      </div>
      <div>
        <input type="submit" :value="text.button" />
      </div>
    </form>
  </div>
</template>

<style scoped>
.content {
  background-color: grey;
  border-radius: 30px;
  padding: 2em;
}

h2 {
  font-size: 3em;
  color: blue;
}

form {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-end;
  gap: 3em;
}
form div {
  display: flex;
  flex-direction: column;
}
form div:first-child {
    flex-grow: 1;
}
form div:first-child * {
  padding: 0.5%;
  margin: 8px 0 8px 0;
  border: 2px solid black;
  border-radius: 4px;
  background-color: white;
}
form div:last-child * {
  padding: 1.5em 2em 1.5em 2em;
  margin: 8px 0 8px 0;
  border: 2px solid black;
  border-radius: 4px;
  background-color: white;
}
</style>

<script>
import { Form } from "../lang/en.js";
export default {
  name: "Contact",
  data(){
    return {
      text: new Form()
    }
  }
};
</script>