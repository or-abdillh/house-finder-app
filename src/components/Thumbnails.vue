<template>
   </template>

<style>
   
   
</style>

<script setup>
   
   import { ref, defineEmits } from 'vue'
   
   
   
   const emits = defineEmits(['change-img'])
   const changeImg = () => {
      emits('change-img', true)
   }
</script>