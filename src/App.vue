<template>
   <Home v-if="isHome" v-on:change-tab="changeTab('home')" ></Home>
   <Details v-if="isDetails" v-on:change-tab="changeTab('details')" ></Details>
</template>

<script setup >
   
   import Home from './views/Home.vue'
   import Details from './views/Details.vue'
   import { ref } from 'vue'
   
   const isHome = ref(true)
   const isDetails  = ref(false)
   
   const changeTab = tab => {
      switch (tab) {
         case 'home' : [ isHome.value, isDetails.value ] = [ false, true ]
         break;
         case 'details' : [ isHome.value, isDetails.value ] = [ true, false ]
      }
   }
</script>

<style>
   
   * {
      font-family: 'Poppins', Sans-Serif;
      user-select: none;
   }
   
</style>