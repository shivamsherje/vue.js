<template>
  <div class="chatbox"></div>
  <div>
    <input type="text" placeholder="Ask a question" />
    <button>Send</button>
  </div>
</template>
<script>
export default {
  name: "Chatbox",
  setup() {},
};
</script>
<style scoped>
.chatbox {
  width: 99%;
  height: 300px;
  overflow-y: scroll;
}
input {
  width: 80%;
  padding: 10px;
}
button {
  padding: 10px;
  width: 10%;
}
</style>
