<template>
   <Preview v-on:change-tab="changeTab()"></Preview>
   <Descriptions></Descriptions>
</template>

<script setup >
   
   import { defineEmits } from 'vue'
   import Preview from '../components/Preview.vue'
   import Descriptions from '../components/Descriptions.vue'
   
   const emits = defineEmits(['change-tab'])
   const  changeTab = () => {
      emits('change-tab')
   }
   
</script>