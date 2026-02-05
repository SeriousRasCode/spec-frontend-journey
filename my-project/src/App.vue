<script setup>
import { ref } from 'vue'
import UserCard from './components/UserCard.vue'
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

<!--day 2 challenge -->
<h1 v-if="name">
    Greetings {{ name }}!
  </h1><br><br>
<input v-model="name" placeholder="Enter your name">
<br><br>

  <!--
  h1 v-else="hint">
    አትፈር
  </h1>
  -->
<!--day 3 challenge -->
  <UserCard name="Tedros" role="Admin" />
</template>