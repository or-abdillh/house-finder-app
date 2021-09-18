<template>
   <Preview v-on:change-tab="changeTab()"></Preview>
</template>

<script setup >
   
   import { defineEmits } from 'vue'
   import Preview from '../components/Preview.vue'
   
   const emits = defineEmits(['change-tab'])
   const  changeTab = () => {
      emits('change-tab')
   }
   
</script>