<script setup>
    console.info("Helo vue");
    const helu = "<h1>Hello Vue</h1>";
    const data = {
        class: "hello",
        id: "hello"
    };
    const buttonDisable = true;

    function helloFunction() {
        return "Hello World";
    }
</script>

<template>
    <h1 v-bind="data">{{helu.toUpperCase()}}</h1>
    <h2>{{ 100 * 200 }}</h2>
    <h2>{{ helloFunction() }}</h2>
    <div :class="data.class" v-html="helu"></div>
    <button :disabled="buttonDisable">This is Button</button>
</template>

<style scoped>
    .hello {
        color: green;
    }
</style>