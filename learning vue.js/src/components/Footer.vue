<template>
  <div class="footer-container">
    <h2>Powered by Llama</h2>
    <a v-bind:href="myLlama">www.myllama.co</a>
    <div class="footer-child-container">
      <p>Disclaimer</p>
      <p>Privacy Policy</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Footer",
  data() {
    return {
      myLlama: "https://www.myllama.co/",
    };
  },
};
</script>
<style scoped>
.footer-container {
  background-color: #f79311;
  width: 99%;
  margin: auto;
  margin-top: 10px;
  padding: 5px;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px,
    rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 10px;
  cursor: pointer;
  color: white;
}
a {
  text-decoration: none;
  color: white;
}
.footer-child-container {
  display: flex;
  gap: 30px;
  justify-content: center;
}
</style>
