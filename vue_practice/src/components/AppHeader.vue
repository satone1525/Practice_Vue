<script setup>
defineProps(['color'])
</script>

<template>
    <header>
        <h1 v-bind:style= "{color:color}"><slot>No Tytle</slot></h1>
    </header> 
</template>