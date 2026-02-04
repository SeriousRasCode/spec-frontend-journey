<script setup>
import { ref } from 'vue'
const name = ref('')
</script>

<template>
  <!--
  <input v-model="name" placeholder="Type your name">
  <p>Hello {{ name }}</p>

  <ul>
  <li v-for="lang in ['JS','Python','Go','Dart','PHP']" :key="lang">
    {{ lang }}
  </li>
</ul>-->

<!--todays challenge -->
<input v-model="name" placeholder="Enter name">
<h1 v-if="name">
    Greetings {{ name }}!
  </h1>
</template>