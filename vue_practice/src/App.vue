<script setup>
import AppHeader from './components/AppHeader.vue'    //コンポーネントをインポート
import TodoList from './components/TodoList.vue'
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
<AppHeader color = 'red'> My ToDo </AppHeader>
<input type="text" size="30" v-model="nweTodo">
<button @click="addTodo()"> 追加 </button>  

<TodoList :todos="todos" @removeTodo='removeTodo'/>
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
