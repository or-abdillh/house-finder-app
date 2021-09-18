<template>
   <Home v-if="isHome" v-on:change-tab="changeTab('home')" ></Home>
</template>

<script setup >
   
   import Home from './views/Home.vue'
   import Details from './views/Details.vue'
   import { ref } from 'vue'
   
   const isHome = ref(true)
   const changeTab = tab => {
      alert(tab)
      switch (tab) {
         case 'home' : isHome.value = false
      }
   }
</script>

<style>
   
   * {
      font-family: 'Poppins', Sans-Serif;
      user-select: none;
   }
   
</style>