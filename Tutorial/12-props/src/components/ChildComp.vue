<template>
  <h3>{{msg || 'No props passed yet'}}</h3>
</template>

<script setup>
// eslint-disable-next-line no-unused-vars,no-undef
const props = defineProps({
  msg: String
})
</script>