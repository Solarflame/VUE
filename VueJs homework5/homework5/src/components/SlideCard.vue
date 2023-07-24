<template>
  <div class="card">
    <div @click="emits(`prev`, props.slideId)" class="button" id="prev">⏩</div>
    <div>
      <h3>{{ props.title }}</h3>
      <h5>{{ props.body }}</h5>
    </div>
    <div @click="emits('next', props.slideId)" class="button" id="next">⏩</div>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title: string
  body: string
  slideId: number
}
const props = defineProps<Props>()

interface Emits{
  (e:'next', id:number):void
  (e:'prev', id:number):void
}
const emits = defineEmits<Emits>()
</script>

<style scoped>
.card {
  color: black;
  border: 1px solid white;
  border-radius: 5px;
  width: 500px;
  height: 300px;
  background-color: yellow;
  display: flex;
  align-items: center;
  justify-content: space-between;

}
.button {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 15px;
  width: 100px;
  height: 40px;
  background-color: rgb(55, 138, 186);
  border-radius: 5px;
  cursor: pointer;
}
#prev{
    rotate: 180deg;
}
</style>
