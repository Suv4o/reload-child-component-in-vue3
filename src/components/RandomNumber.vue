<script setup>
import { ref, onMounted } from "vue";

const randomNumber = ref(0);

onMounted(() => {
    randomNumber.value = Math.floor(Math.random() * 100);
});
</script>

<template>{{ randomNumber }}</template>

<style scoped></style>
