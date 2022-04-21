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
