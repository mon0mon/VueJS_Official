<template>
  <h2>Child component</h2>
</template>

<script setup>
// eslint-disable-next-line no-undef,no-unused-vars
const emit = defineEmits(['response'])

emit('response', 'hello')
</script>