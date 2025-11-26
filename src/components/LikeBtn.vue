<script setup>
import { ref } from "vue";
const bgRed = ref(false);
</script>
<template>
  <div>
    <button @click="bgRed = !bgRed" style="background: none; border: none;" >{{ bgRed ? '❤' :  '🤍' }}</button>
  </div>
</template>

<style scoped></style>
