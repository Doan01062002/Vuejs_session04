<template>
  <div>
    <h3>Giỏ hàng</h3>
    <ul>
      <li>
        Mèn mén loại 1 - số lượng: {{ opt1 }}
        <button @click="changeValue1">Tăng số lượng</button>
      </li>
      <li>
        Mèn mén loại 2 - số lượng: {{ opt2 }}
        <button @click="changeValue2">Tăng số lượng</button>
      </li>
      <li>
        Mèn mén loại 3 - số lượng: {{ opt3 }}
        <button @click="changeValue3">Tăng số lượng</button>
      </li>
    </ul>
    <p>Tổng số lượng sản phẩm: {{ sum }}</p>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";

let opt1 = ref(0);
let opt2 = ref(1);
let opt3 = ref(2);
const sum = computed(() => opt1.value + opt2.value + opt3.value);

const changeValue1 = () => {
  opt1.value++;
};
const changeValue2 = () => {
  opt2.value++;
};
const changeValue3 = () => {
  opt3.value++;
};
</script>

<style></style>
