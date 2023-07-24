<template>
  <div>
    <select id="random">
      <option value="list">in turn</option>
      <option value="random">random</option>
    </select>
    <div class="block" v-random="materials"></div>
  </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const materials = ref({
  img: [
    'https://bipbap.ru/wp-content/uploads/2018/06/img_resize.jpg',
    'https://klike.net/uploads/posts/2018-12/1544425294_2.jpg',
    'https://klike.net/uploads/posts/2018-12/1544425315_3.jpg',
    'https://klike.net/uploads/posts/2018-12/1544425270_1.jpg'
  ],
  timeout: 3000
})
 console.log(materials.value)
</script>

<style scoped>
.block{
  width: 500px;
  height: 500px;
  background-color: aqua;
  border: 3px solid rgb(23, 186, 69);
}

</style>