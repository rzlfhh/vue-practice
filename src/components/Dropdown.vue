<template>
  <div class="dropdown">
    <button @click="showDropdown">Dropdown</button>

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

<style lang="scss" scoped>
@mixin border {
  border: 1px solid rgb(182, 182, 182);
}

@mixin fade-in {
  opacity: 1;
  animation-name: fadeInOpacity;
  animation-iteration-count: 1;
  animation-timing-function: ease-in;
  animation-duration: 0.2s;
}

@keyframes fadeInOpacity {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.dropdown {
  position: relative;
}

button {
  background: white;
  @include border();
  border-radius: 24px;
  padding: 0.8em 2em;
  cursor: pointer;
  justify-content: end;
}

.dropdown-menu {
  width: fit-content;
  @include border();
  margin-top: 0.5em;
  border-radius: 12px;
  padding: 2em 1.8em;
  @include fade-in();

  ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    li {
      margin-bottom: 1.5rem;

      &:last-child {
        margin-bottom: 0;
      }
    }
  }
}
</style>
