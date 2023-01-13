<template>
  <input :value="text" @input="onInput" placeholder="Type here">
  <p>{{ text }}</p>
  <input v-model="text2" placeholder="Type here">
  <p>{{ text2}}</p>
</template>

<script setup>
import {ref} from "vue";

const text = ref('')
const text2 = ref('')

// eslint-disable-next-line no-unused-vars
function onInput(e) {
  text.value = e.target.value
}

</script>