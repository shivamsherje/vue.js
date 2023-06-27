<template>
  <div>
    <div class="modal" v-if="showModal">
      <div class="modal-content">
        <div style="text-align: right">
          <button style="
              border: none;
              background-color: white;
              color: #f79311;
              font-size: 30px;
              font-weight: bolder;
            " class="close-button1" @click="closeModal">
            ×
          </button>
        </div>

        <h1>Disclaimer</h1>
        <br />
        <hr />
        <br />

        <p>
          This is a research project, might give incorrect and irrelevant
          answers sometimes.
        </p>
        <br />

        <hr />
        <button class="close-button2" @click="closeModal">CLOSE</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Disc",
  data() {
    return {
      showModal: true,
    };
  },
  methods: {
    closeModal() {
      this.showModal = false;
    },
  },
};
</script>

<style>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal-content {
  background-color: #fff;
  padding: 20px;
  border-radius: 4px;
  text-align: center;
  box-shadow: rgba(215, 214, 212, 0.915) 0px 22px 70px 4px;
}

.close-button2 {
  width: 100%;
  border-radius: 30px;
  border: none;
  background-color: #f79311;
  color: white;
  padding: 2px;
  margin-top: 20px;
  font-weight: bold;
}

.close-button1 {
  text-align: right;
}
</style>
