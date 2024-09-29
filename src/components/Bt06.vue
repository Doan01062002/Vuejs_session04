<template>
  <div>
    <h3>Giỏ hàng</h3>

    <input
      type="number"
      v-model.number="inputValue"
      placeholder="Nhập số tiền"
    />

    <button @click="addToCart">Add to cart</button>

    <p>Tổng tiền trong giỏ hàng: {{ totalCartValue }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const inputValue = ref(0);

const totalPrice = ref(0);

const totalCartValue = computed(() => totalPrice.value);

const addToCart = () => {
  totalPrice.value += inputValue.value;

  inputValue.value = 0;
};
</script>

<style scoped>
input {
  margin-bottom: 10px;
  padding: 8px;
  font-size: 16px;
}
button {
  padding: 8px 16px;
  background-color: dodgerblue;
  color: white;
  border: none;
  cursor: pointer;
}
</style>
