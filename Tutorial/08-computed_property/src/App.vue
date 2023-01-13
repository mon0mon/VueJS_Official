<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Add Todo</button>
  </form>
  <form>
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done">
      <span :class="{marked_done: todo.done}">{{todo.text}}</span>
      <button @click="removeTodo(todo)">&Cross;</button>
    </li>
  </form>
  <button @click="hideCompleted = !hideCompleted">
    {{hideCompleted ? 'Show all' : 'Hide completed'}}
  </button>
</template>

<script setup>

import {computed, ref} from "vue";

let id = 0

const newTodo = ref('')
const hideCompleted = ref(false)
const todos = ref ([
  {id: id++, text: 'Learn HTML', done: true},
  {id: id++, text: 'Learn JavaScript', done: true},
  {id: id++, text: 'Learn Vue', done: false},
])
const filteredTodos = computed(() => {
  return hideCompleted.value
    ? todos.value.filter((t) => !t.done) : todos.value
})

function addTodo() {
  todos.value.push({id: id++, text: newTodo.value, done: false})
  newTodo.value = ''
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}

</script>

<style scoped>
.marked_done {
  text-decoration: line-through;
}
</style>