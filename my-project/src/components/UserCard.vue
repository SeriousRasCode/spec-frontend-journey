<template>
  <div class="card">
    <h1>{{ name }}</h1>
    <p>{{ role }}</p>
  </div>
</template>

<script>
export default {
  props: ['name', 'role']
}
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
</style>