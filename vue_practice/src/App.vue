<script setup>
import { ref, computed } from 'vue'

/*
const answer = computed(() => {
  return 123 + 456
})
*/

const message = computed(() =>{
  return 'ようそこ！ <strong>'+myname.value+'</strong>さん'
})
const welcomeColor = 'blue'
const myname = ref('')
</script>

<template>
<h1>Vue 3</h1>
<p>お名前は？: <input type="text" size="30" v-model="myname"></p>
<p v-html="message" :style="{ 'background-color':welcomeColor, 'color':'white' }"></p>
</template>