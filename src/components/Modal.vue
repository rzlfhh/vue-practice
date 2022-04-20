<template>
  <div class="modal-overlay" @click="$emit('close-modal')">
    <div class="modal" @click.stop>
      <img src="../assets/images/success.svg" alt="modal image" />
      <h6>Message Title</h6>
      <p>
        Lorem ipsum doler sit amet, Lorem ipsum doler sit amet, Lorem ipsum
        doler sit amet Lorem ipsum doler sit amet Lorem ipsum doler sit amet
        Lorem ipsum doler sit amet
      </p>
      <Button @click="$emit('close-modal')">close</Button>
    </div>
  </div>
</template>

<script setup>
import Button from "./Button.vue";
</script>

<style lang="scss" scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  background-color: #1b1b1bda;
  display: grid;
  place-content: center;
}

.modal {
  text-align: center;
  background-color: white;
  height: fit-content;
  width: 600px;
  padding: 3em;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;

  img {
    width: 240px;
    margin-bottom: 1.5em;
  }

  h6 {
    font-weight: 500;
    font-size: 20px;
    margin-bottom: 1em;
  }

  p {
    font-size: 12px;
    margin-bottom: 2em;
  }

  button {
    background: transparent;
    border: 1px solid rgb(255, 130, 130);
    color: rgb(255, 130, 130);
  }
}
</style>
