<template>
  <div>
    <button @click="decrement">-</button>

    <span> Current value: {{ count }} </span>

    <button @click="increment">+</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0);

// добавим методы для изменения переменной count.

/* Метод уменьшения значения */
const decrement = () => {
  count.value = count.value - 1;
};

/* Метод увеличения значения */
const increment = () => {
  count.value = count.value + 1;
};
</script>

<style>
body {
  padding: 50px;
}

div {
  display: flex;
  gap: 1em;
  align-items: center;
  width: fit-content;
}

button {
  padding: 3px 1em;
  border: 2px solid deepskyblue;
  font-family: inherit;
  background: white;
}
</style>
