<script setup>
import { ref } from 'vue';
import NewTodoInput from './components/NewTodoInput.vue';
import ListTodo from './components/ListTodo.vue';

/** array with reactive  */
const list = ref([]);

/**
 * Function passed with param to props createTodo
 * @param {*} item 
 */
function addTodo(item) {
  list.value.push(item)
}
</script>

<template>
  <NewTodoInput :createTodo="addTodo" />
  <ListTodo :todoItems="list"/>
</template>

