<template>
  <div>
    <h3>Tính bình phương của một số</h3>

    <input type="number" v-model.number="number" placeholder="Nhập một số" />

    <p>Bình phương của số: {{ squaredValue }}</p>
  </div>
</template>

<script setup>
import { ref, computed, watch } from "vue";

const number = ref(0);

const squaredValue = computed(() => number.value * number.value);

watch(number, (newValue, oldValue) => {
  console.log(`Giá trị đã thay đổi từ ${oldValue} sang ${newValue}`);
});
</script>

<style scoped>
input {
  margin-bottom: 10px;
  padding: 8px;
  font-size: 16px;
}
</style>
