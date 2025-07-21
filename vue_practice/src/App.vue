<script setup>
import { ref } from 'vue'
const number = ref(0)
const add = () => {
  number.value++
}
</script>
<template>
<input type="text" size="30" v-model="number">
<button @click="add()"> +1 </button>  
</template>

<!--　省略形　メモ 
・v-bind → :
・v-on → @ 
-->

<!-- template をコメントアウト 2つ目の動画終了 -->
<!--
<template>
  <h1>Vue 3</h1>
  ...
</template>
-->

<!-- script をコメントアウト 2つ目の動画終了時にはここがscript setupだった-->
<!--
// import { ref, computed } from 'vue'
// const myname = ref('')
// const message = computed(() => 'ようそこ！ <strong>' + myname.value + '</strong>さん')
// ...
-->
