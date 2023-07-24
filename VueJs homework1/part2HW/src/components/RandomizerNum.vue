<template>
  <div>
    <p>Random number: {{ randomNum }}</p>
    <input id="endpoint" type="number" placeholder="">
    <button @click="create">GO</button>
  </div>
</template>

<script setup>
    import {ref} from "vue"
    let randomNum = ref()
    const history = []
    const create = () =>{
      let endpoint = +document.querySelector('#endpoint').value
      let random = Math.floor(Math.random()*endpoint)
      randomNum.value = random
      history.push(random)
      console.log(history)
    }
</script>

<style scoped></style>
