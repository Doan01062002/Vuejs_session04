<!-- <template>
  <div>
    <h3>Name: {{ user.name }}</h3>
    <h3>Age: {{ user.age }}</h3>
    <button @click="handleClick">Increase Age</button>
    <p>************* computed *****************</p>
    <p>numberCount {{ numberCount }}</p>
    <p>numberCount mũ 2: {{ caculator }}</p>
    <button @click="handleClickNumberCount">click</button>
    <p>****************** watchers ***************</p>
    <p>{{ number }}</p>
    <button @click="handleClickIncrease">increse</button>
  </div>
</template>
<script setup>
import { computed, reactive, ref, watch } from "vue";

// Reactive
const user = reactive({
  id: 1,
  name: "Đoan",
  age: 22,
});

const handleClick = () => {
  user.age++;
};
// Computed
const numberCount = ref(5);

const caculator = computed(() => numberCount.value ** 2);

const handleClickNumberCount = () => {
  numberCount.value *= 2;
};

// Watchers
const number = ref(1);
watch(number, (newValue, oldValue) => {
  // Thường được sử lý để call API
  console.log("giá trị newValue", newValue);
  console.log("giá trị oldValue", oldValue);
});

const handleClickIncrease = () => {
  number.value++;
};
</script>
<style scoped></style> -->

<template>
  <div>
    <Bt01></Bt01>
    <Bt02></Bt02>
    <Bt03></Bt03>
    <br />
    <Bt04></Bt04>
    <br />
    <Bt05></Bt05>
    <br />
    <Bt06></Bt06>
    <br />
    <Bt07></Bt07>
    <br />
    <Bt08></Bt08>
  </div>
</template>
<script setup>
import Bt01 from "./components/Bt01.vue";
import Bt02 from "./components/Bt02.vue";
import Bt03 from "./components/Bt03.vue";
import Bt04 from "./components/Bt04.vue";
import Bt05 from "./components/Bt05.vue";
import Bt06 from "./components/Bt06.vue";
import Bt07 from "./components/Bt07.vue";
import Bt08 from "./components/Bt08.vue";
</script>
<style></style>
