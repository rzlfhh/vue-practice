<script setup>
import { reactive, ref } from "@vue/reactivity";

let counterData = reactive({
  counter: 0,
  title: "my counter",
});

const isRed = ref(false);

const toRed = () => {
  isRed.value = !isRed.value;
};

const increaseCounter = () => {
  counterData.counter++;
};

const decrease = () => {
  counterData.counter--;
};
</script>

<template>
  <h1>{{ counterData.title }}</h1>
  <div class="wrapper-counter">
    <button @click="decrease">-</button>
    <span>{{ counterData.counter }}</span>
    <button @click="increaseCounter">+</button>
  </div>

  <div>
    <h2>edit title</h2>
    <input v-model="counterData.title" type="text" />
  </div>

  <h3 :class="{ red: isRed }" @click="toRed">click to make red</h3>
</template>

<style scoped>
.wrapper-counter {
  text-align: center;
  font-size: 2rem;
  display: flex;
  gap: 1em;
  justify-content: center;
}

button {
  font-size: 2rem;
  height: 4rem;
  width: 4rem;
}

.red {
  color: red;
}
</style>
