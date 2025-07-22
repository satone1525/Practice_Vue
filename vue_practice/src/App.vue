<script setup>
import { ref } from 'vue'

const todos = ref([])
const nweTodo = ref('')

const addTodo = () => {
  todos.value.push(nweTodo.value)
  nweTodo.value = ''
}

const removeTodo = (index) => {
  todos.value.splice(index, 1)    //要素から1つ消す
}

</script>

<template>
<input type="text" size="30" v-model="nweTodo">
<button @click="addTodo()"> 追加 </button>  

<ul v-if="todos.length > 0">
  <li v-for="(todo, i) in todos" v-bind:key="i"> {{ todo }} <span @click="removeTodo(i)" style="cursor:pointer"> x </span> </li>

</ul>
<p v-else>※ToDoを追加してください</p>
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
-->

<!-- script をコメントアウト 3つ目の動画終了時にはここがscript setupだった (ボタンクリックすると数が増える)  -->
<!--
// import { ref } from 'vue'
// const number = ref(0)
// const add = () => {
//   number.value++
// }
-->
