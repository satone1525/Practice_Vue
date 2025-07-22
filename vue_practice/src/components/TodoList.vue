<script setup>
defineProps(['todos'])
const emit = defineEmits(['removeTodo'])

const clickRemove = (i) => emit('removeTodo', i)    //クリックされたのを通知するためのイベント
</script>

<template>
<ul v-if="todos.length > 0">
  <li v-for="(todo, i) in todos" v-bind:key="i"> {{ todo }} <span @click="clickRemove(i)" style="cursor:pointer"> x </span> </li>

</ul>
<p v-else>※ToDoを追加してください</p>
</template>