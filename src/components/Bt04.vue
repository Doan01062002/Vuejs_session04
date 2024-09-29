<template>
  <div>
    <input
      type="text"
      v-model="inputValue"
      placeholder="Nhập giá trị vào đây"
    />
  </div>
</template>

<script setup>
import { ref, watch } from "vue";

const inputValue = ref("");

watch(inputValue, (newValue, oldValue) => {
  console.log(`Giá trị đã thay đổi từ ${oldValue} sang ${newValue}`);
});
</script>

<style scoped>
input {
  padding: 8px;
  font-size: 16px;
}
</style>
