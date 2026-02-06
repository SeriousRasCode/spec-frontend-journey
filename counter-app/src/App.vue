<script setup>
import { ref } from 'vue';
const count = ref(0);

const increase = () => {
  count.value++;
};

const decrease = () => {
    count.value--;
  
};
</script>

<template>
  <div class="c-cont">
    <h2>My Counter</h2>
    
    <h1>{{ count }}</h1>

    <div>
      <button @click="decrease" :disabled="count === 0">—</button>
      <button @click="increase">+</button>
    </div>
  </div>
</template>

<style scoped>
.c-cont {
  border: 1px solid #ffdeb2;
  border-radius:12px;
  padding: 20px;
  text-align: center;
  margin-top: 50px;
}
h1 {
  font-size: 48px;
}
button {
  color:#ccc;
  border-radius: 20%;
  border-color: #ffdeb2;
  border-width: 1px;
  width:60px;
  height:60px;
  background-color: transparent;
  padding: 10px 20px;
  font-size: 18px;
  margin: 0 10px;
  cursor: pointer;
}
button:disabled {
  cursor:not-allowed;
  opacity: 0.2;
}
</style>