<template>
  <div>
    <p>Company: {{ check === false ? edu.company : academy.company }}</p>
    <p>Age: {{ check === false ? edu.age : academy.age }}</p>
    <button @click="handleChange">Change data</button>
  </div>
</template>
<script setup>
import { ref } from "vue";

const edu = ref({
  company: "Rikkei Education",
  age: 1,
});
const academy = ref({
  company: "Rikkei Academy",
  age: 2,
});
const check = ref(false);
const handleChange = () => {
  check.value = !check.value;
};
</script>
<style></style>
