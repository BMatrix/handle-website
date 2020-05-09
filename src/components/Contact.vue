<template>
  <div class="content">
    <h2>Contact form</h2>
    <form>
      <div>
        <input type="text" placeholder="First name" required />
        <input type="text" placeholder="Last name" required />
        <input type="email" placeholder="Email" required />
        <input type="text" placeholder="Company (Optional)" />
        <textarea rows="4" placeholder="Message" required />
      </div>
      <div>
        <input type="submit" value="Send" />
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
export default {
  name: "Contact"
};
</script>