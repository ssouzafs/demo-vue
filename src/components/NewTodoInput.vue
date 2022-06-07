<script setup>
import { ref } from 'vue';

/** property reactive */
const newTodo = ref('');

/** property in the work how a function */
const { createTodo } = defineProps({
  createTodo: Function
});

/**
 * capture submit of form
 * case input is not empty add in method createTodo
 */
function handleSubmit() {
  if (newTodo.value) {
    createTodo(newTodo.value)
    newTodo.value = ''
  }
}

</script>

<template>
  <label for="todo">Novo TODO:</label>
  <input id="todo" v-model="newTodo">
  <button @click="handleSubmit">Add</button>
</template>

<style scoped>
input {
  height: 20px;
  margin-left: 5px;
}

button {
  height: 27px;
  width: 80px;
  cursor: pointer;
}
</style>