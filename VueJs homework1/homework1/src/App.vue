<template>
  <div>      
    <h1>User Info</h1>
    <p>ID: {{ user.Id }}</p>
    <p>Name: {{ user.Name }}</p>
    <p>Surname: {{ user.Surname }}</p>
    <p>Age: {{ user.Age }}</p>
    <p>Email: {{ user.Mail }}</p>
    <p>Country: {{ user.Country }}</p>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  const user = ref({
	Id: 525,
	Name: "Yeldos",
	Surname: "Abdibekov",
	Age: 24,
	Mail: "abdibekov.eldos@gmail.com",
	Country: "Kazakhstan",
})

</script>

<style scoped>

</style>
