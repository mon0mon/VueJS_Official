<template>
  <ol>
    <TodoItem v-for="item in groceryList" :todo="item" :key="item.id"></TodoItem>
  </ol>
</template>

<script setup>

import TodoItem from "@/components/TodoItem.vue";
import {ref} from 'vue';

const groceryList = ref([
  {id: 0, text: 'Vegetables'},
  {id: 1, text: 'Cheese'},
  {id: 2, text: 'Whatever else humans are supposed to eat'}
])

</script>

<style>
</style>
