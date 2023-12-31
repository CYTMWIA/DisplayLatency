<template>
    <div>
        <div class="bar full"></div>
        <div class="bar progress" :style="{ width: peroid }"></div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const peroid = ref("100%")

setInterval(() => {
    let n = ((Date.now() % 1000) / 1000) * 100
    peroid.value = n.toString() + "%"
}, 1)

</script>

<style scoped>
.bar {
    height: 1em;
    width: 100%;
    margin-left: 0;
    margin-right: auto;
}

.full {
    background-color: rgb(255, 0, 0);
}

.progress {
    background-color: rgb(0, 255, 0);
}
</style>
