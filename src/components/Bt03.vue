<template>
  <div>
    <p>Acreage: {{ S }}</p>
    <button @click="handleChange">Change data</button>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const width = ref(10);
const height = ref(20);

const S = computed(() => width.value * height.value);

const handleChange = () => {
  width.value += 10;
};
</script>

<style></style>
