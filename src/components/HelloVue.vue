<script setup>
    console.info("Helo vue");
    const helu = "<h1>Hello Vue</h1>";
    const data = {
        class: "hello",
        id: "hello"
    };
    const buttonDisable = true;
</script>

<template>
    <h1 v-bind="data">{{ helu}}</h1>
    <div :class="data.class" v-html="helu"></div>
    <button :disabled="buttonDisable">This is Button</button>
</template>

<style scoped>
    .hello {
        color: green;
    }
</style>