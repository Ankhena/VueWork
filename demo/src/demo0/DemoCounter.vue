<template>
  <div class="counter">
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
</style>

<style lang="scss" scoped>
.counter {
  display: flex;
  gap: 1em;
  align-items: center;
  width: fit-content;

  button {
    margin: 0 10px;
    font-size: 1.5rem;
    width: 2rem;
    height: 2rem;
    border-radius: 50%;
    border: none;
    background: #dd0000;
    color: white;
    cursor: pointer;

    &:hover {
      background: #ff0000;
    }
  }
}
</style>
