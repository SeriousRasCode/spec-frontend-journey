<template>
  <!--div with conditional coloring using ternary operator-->
  <div class="card" :style="{ borderColor: status === 'online' ? 'green' : 'red' }">

    <p v-if="status === 'online'">🟢 Online</p>
    <p v-else>🔴 Offline</p>

    <h1>{{ name }}</h1>
    <p>{{ role }}</p>

    <button @click="$emit('view-profile', name)">
      View Profile
    </button>
  </div>
</template>

<script setup>
defineProps(['name', 'role', 'status'])
defineEmits(['view-profile'])
</script>

<style lang="css">


.card {
  border: 2px solid #ffc05a;
  padding: 20px;
  border-radius: 8px;
  width: 200px;
  text-align: center;
  font-family: sans-serif;
}

h1 {
  margin: 0;
  font-size: 1.5rem;
}

p {
  color: rgb(245, 168, 25);
  margin: 5px 0 0 0;
}

button{
  margin-top: 10px;
  color: white;
  background-color: transparent;
  padding: 8px;
  border-radius: 8px;
  text-align: center;
  font-family: sans-serif;
}
</style>