<template>
  <Timer id="timer" />
  <TimerBar id="timer_bar" />
</template>

<script setup lang="ts">
import Timer from "./components/Timer.vue";
import TimerBar from "./components/TimerBar.vue";
</script>

<style scoped>
#timer {
  font-size: 15vh;
  width: max-content;
  margin: auto auto;
}

#timer_bar {
  margin: auto auto;
  width: 80vw;
}
</style>
