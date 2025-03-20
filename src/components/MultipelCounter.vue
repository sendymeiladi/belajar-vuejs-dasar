<script setup>

import { ref } from "vue";
import Counter from "./Counter.vue";
import CounterStatless from "./CounterStatless.vue";

const name1 = "Sendy";
const name2 = "Meiladi";

const counter = ref(0);
</script>

<template>
    <Counter :name="name1" initial-counter="10"/>
    <Counter v-bind:name="name2" initial-counter="20"/>

    <CounterStatless name="Deri" :counter="counter" />
    <CounterStatless name="Rudi" :counter="counter" />
    <button @click="counter++">Increment Counter</button>
</template>

<style scoped>

</style>