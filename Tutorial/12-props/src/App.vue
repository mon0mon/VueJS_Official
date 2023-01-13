<template>
  <ChildComp :msg="greeting"></ChildComp>
</template>
<script setup>
import ChildComp from "@/components/ChildComp.vue";
import {ref} from "vue";

const greeting = ref('Hello')
</script>