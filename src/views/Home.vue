<template>
   <Navbar></Navbar>
   <Searchbar></Searchbar>
   <Category></Category>
   <Card v-on:change-tab="changeTab()" ></Card>
</template>

<style>
   
</style>

<script setup >
   
   import Navbar from '../components/Navbar.vue'
   import Searchbar from '../components/Searchbar.vue'
   import Category from '../components/Category.vue'
   import Card from '../components/Card.vue'
   import { defineEmits } from 'vue'
   
   const emits = defineEmits(['change-tab'])
   
   const changeTab = () => {
      emits('change-tab')
   }
   
</script>