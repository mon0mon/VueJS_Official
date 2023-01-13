<template>
<!--  <ChildComp>Messsage : {{msg}}</ChildComp>-->
  <ChildComp></ChildComp>
</template>
<script setup>
import ChildComp from "@/components/ChildComp.vue";
import {ref} from "vue";

// eslint-disable-next-line no-unused-vars
const msg = ref('from parent')
</script>