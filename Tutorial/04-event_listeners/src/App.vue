<template>
  <button @click="onClickButton">count is : {{count}}</button>
</template>

<script setup>
import {ref} from "vue";

const count = ref(0);

function onClickButton() {
  count.value++;
}
</script>