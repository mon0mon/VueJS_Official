<template>
  <ChildComp @response="(msg) => childMsg = msg"></ChildComp>
  <p>{{childMsg}}</p>
</template>

<script setup>

import {ref} from "vue";
import ChildComp from "@/components/ChildComp.vue";

const childMsg = ref('No child msg yet')
</script>
