<script setup>
const { todoItems } = defineProps({
  todoItems: Array
})
</script>
<template>
  <ul>
    <li v-for="item in todoItems" :key="item">{{ item }}</li>
  </ul>
</template>