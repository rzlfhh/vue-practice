<script setup>
import Counter from "../components/Counter.vue";
import Dropdown from "../components/Dropdown.vue";
import Button from "../components/Button.vue";
import Modal from "../components/Modal.vue";

import { ref } from "@vue/reactivity";

let showModal = ref(false);

// const openModal = () => {
//   showModal.value = !showModal.value;
// };
</script>

<template>
  <main>
    <h1>home page</h1>

    <Counter />
    <div class="container-dropdown">
      <Dropdown />
      <Dropdown />
    </div>
    <Button @click="showModal = true"> Open Modal </Button>
    <Modal v-show="showModal" @close-modal="showModal = false" />
  </main>
</template>

<style lang="scss" scoped>
.container-dropdown {
  display: flex;
  gap: 1em;
  width: 100%;
  margin-bottom: 2em;
}
</style>
