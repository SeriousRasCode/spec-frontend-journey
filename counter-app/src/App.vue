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
  
  padding: 20px;
  text-align: center;
  margin-top: 50px;
}
h1 {
  font-size: 48px;
}
button {
  width: 60px;
  height: 40px;
  margin: 0 10px;
  cursor: pointer;
  background: none;
  color: #ffdeb2;
  border: 1px solid #ffdeb2;
  border-radius: 12px;
  transition: 0.2s;
}

button:hover:not(:disabled) {
  background: #ffdeb2;
  color: #222;
}

button:disabled {
  opacity: 0.3;
  cursor: not-allowed;
}
</style>