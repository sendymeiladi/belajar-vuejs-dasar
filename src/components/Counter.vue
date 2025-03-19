<script setup>
    import { nextTick, ref } from 'vue';
    console.info(`Load Component`);
    let counter = ref({
        count: 0,
        name: "sendy"
    });

    async function incremenet(){
        console.info(`Increment counter : ${counter.value.count}`);
        counter.value = {
            name: counter.value.name,
            count: counter.value.count + 1
        }

        await nextTick();
        counter.value.count++;
        await nextTick();
        counter.value.count++;
        await nextTick();
        
        console.log("Increment count after nextTrick");
    }
</script>

<template>
    <div>
        <h1 id="count">Counter : {{ counter.count }}</h1>
        <button v-on:click="incremenet">incremenet</button>
    </div>
</template>

<style scoped>

</style>