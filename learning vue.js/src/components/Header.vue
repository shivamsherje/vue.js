<template>
  <div class="header-container">
    <div class="header-child-container">
      <a v-bind:href="myLlama">
        <img
          class="app-logo"
          src="https://www.myllama.co/wp-content/uploads/2023/01/LAMA-logo_Final-01.png"
      /></a>

      <div>
        <h1>Ask Liama</h1>
        <p>Modern Problems. Timeless Answers</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header",
  data() {
    return {
      myLlama: "https://www.myllama.co/",
    };
  },
};
</script>
<style scoped>
.app-logo {
  width: 5em;
  box-shadow: rgba(231, 122, 44, 0.775) 0px 0px 0px 3px;
  border-radius: 50%;
}
.header-container {
  background-color: #f79311;
  width: 97%;
  margin: auto;
  margin-top: 10px;
  padding-top: 1rem;
  padding: 1em;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px,
    rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
  border: 1px solid red;
  cursor: pointer;
  color: white;
}
.header-child-container {
  display: flex;
  gap: 1em;
  margin: auto;
  /* border: 2px solid red; */
  width: 400px;
  justify-content: center;
  align-items: center;
}
.header-child-container > div {
  color: white;
}
.header-child-container > div > p {
  font-size: 20px;
}
.header-child-container > div > h1 {
  font-size: 40px;
}
</style>
