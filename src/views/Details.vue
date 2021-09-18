<template>
   <section class="fade-in">
      <Preview v-on:change-tab="changeTab()"></Preview>
      <Descriptions></Descriptions>
      <Actions></Actions>
   </section>
</template>

<style>
   
   @keyframes fade-in {
      from {
         opacity: .35;
      } to {
         opacity: 1;
      }
   }
   
   .fade-in {
      animation: fade-in .3s forwards;
   }
   
</style>

<script setup >
   
   import { defineEmits } from 'vue'
   import Preview from '../components/Preview.vue'
   import Descriptions from '../components/Descriptions.vue'
   import Actions from '../components/Actions.vue'
   
   const emits = defineEmits(['change-tab'])
   const  changeTab = () => {
      emits('change-tab')
   }
   
</script>