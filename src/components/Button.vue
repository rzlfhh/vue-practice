<template>
  <button>
    <slot />
  </button>
</template>

<script setup></script>

<style lang="scss" scoped>
button {
  background: green;
  color: white;
  border: none;
  padding: 0.8em 2em;
  cursor: pointer;
  border-radius: 24px;
}
</style>
