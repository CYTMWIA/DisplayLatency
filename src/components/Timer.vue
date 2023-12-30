<template>
    <div>
        {{ time_string }}
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

function now_time_string(): string {
    let now = new Date()
    let fixed_width = (x: number, w: number) => x.toString().padStart(w, "0")
    let res = `${fixed_width(now.getHours(), 2)}:${fixed_width(now.getMinutes(), 2)}:${fixed_width(now.getSeconds(), 2)}.${fixed_width(now.getMilliseconds(), 3)}`
    return res
}

const time_string = ref("00:00:00.000")

setInterval(() => {
    time_string.value = now_time_string()
}, 1)

</script>

<style scoped></style>
