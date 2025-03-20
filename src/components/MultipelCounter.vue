<script setup>

import { ref } from "vue";
import Counter from "./Counter.vue";
import CounterStatless from "./CounterStatless.vue";

const name1 = "Sendy";
const name2 = "Meiladi";

const counter = ref(0);

function increment(value){
    counter.value += value;
}
</script>

<template>
    <Counter :name="name1" initial-counter="10"/>
    <Counter v-bind:name="name2" initial-counter="20"/>

    <CounterStatless name="Deri" :counter="counter" :increment="1" v-on:click="increment"/>
    <CounterStatless name="Rudi" :counter="counter" :increment="2" @click="increment"/>
</template>

<style scoped>

</style>