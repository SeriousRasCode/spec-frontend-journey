<script setup>



import { ref } from 'vue'
import UserCard from './components/UserCard.vue'



const name = ref('')

const showAlert = (userName) => {
  alert("Profile of " + userName);
}



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
  <!--<h1 v-if="name">
    Greetings {{ name }}!
  </h1><br><br>
<input v-model="name" placeholder="Enter your name">
<br><br>-->

  <!--
  h1 v-else="hint">
    አትፈር
  </h1>
  -->
  <!--day 3 challenge -->
  <div class="card-cont">
    <UserCard name="Tedros" role="Admin" status="online" @view-profile="showAlert" />
    <UserCard name="Moa" role="Manager" status="offline" @view-profile="showAlert" />
    <UserCard name="Ezana" role="Employee" status="online" @view-profile="showAlert" />
  </div>
</template>

<script>

</script>

<style lang="css">
.card-cont {
  display: flex;
  justify-content: center; 
  align-items: center;     
  gap: 20px;
  min-height: 100vh;       
  width: 100%;
  
}
</style>