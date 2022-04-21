<template>
  <div class="dropdown">
    <button
      class="btn__dropdown"
      @mouseover="showDropdown"
      @mouseout="isOpen = false"
    >
      Dropdown
    </button>

    <div class="dropdown-menu" v-show="isOpen">
      <ul>
        <li>Lorem ipsum dolor sit amet.</li>
        <li>Lorem ipsum dolor sit amet.</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity";

let isOpen = ref(false);
const showDropdown = () => {
  isOpen.value = !isOpen.value;
};
</script>
