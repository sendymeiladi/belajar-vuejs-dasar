<script setup>
    console.info("Helo vue");
    const helu = "<h1>Hello Vue</h1>";
</script>

<template>
    <h1 class="hello">{{ helu}}</h1>
    <div v-html="helu"></div>
</template>

<style scoped>
    .hello {
        color: green;
    }
</style>