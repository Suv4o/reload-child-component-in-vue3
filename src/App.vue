<script setup>
import { ref } from "vue";
import RandomNumber from "./components/RandomNumber.vue";

const keyIndex = ref(0);

function changeKey() {
    keyIndex.value++;
}
</script>

<template>
    <RandomNumber :key="keyIndex" />
    <button @click="changeKey">Re-Render</button>
</template>

<style>
html,
body {
    font-size: 100%;
    overflow-x: hidden;
    align-content: center;
    background-color: #efe8df;
    color: #173353;
    display: grid;
    justify-content: center;
    min-height: 100vh;
    font-size: 80px;
}
*,
*::before,
*::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    line-height: 1.3;
}

button {
    display: block;
    font-size: 24px;
    cursor: pointer;
    border: 0;
    border-radius: 4px;
    padding: 10px 10px;
    background-color: #173353;
    color: #efe8df;
}
</style>
