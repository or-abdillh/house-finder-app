<template>
   <section class="card">
      <template v-for="card in 10">
         <div class="card-wrapper">
           <div class="card-header">
              <img src="/house-finder.jpeg"/>  
              <i @click="btnLike" class="far fa-heart absolute top-3 right-3 text-2xl text-gray-200" data-click="false"></i>
           </div> 
           <div class="card-footer">
           <h1 @click="changeTab()" class="title-card" >The Peninsula Chicago</h1>
           <span>
              <i class="fa fa-bed"></i>
              4
           </span>
           <span>
              <i class="fa fa-bath"></i>
              2
           </span>
           <span>
              <i class="fas fa-chart-area"></i>
               1200 sqft 
           </span>
           <br />
           <strong> $ 1500/month</strong>
        </div> 
      </div>
      </template>
   </section>
</template>

<style>
   
   .card {
      @apply px-5 py-2;
   }
   
   .card-wrapper {
      @apply w-full md:w-10/12 mb-5 mx-auto rounded-2xl overflow-hidden border-2 border-gray-200;
   }
   
   .card-header {
      @apply relative;
   }
   
   .title-card {
      @apply text-xl duration-300 text-gray-600 font-semibold;
   }
   
   .title-card:active {
      letter-spacing: 1.5px;
   }
   
   .card-footer {
      @apply px-5 py-3 bg-gray-100;
   }
   
   .card-footer i {
      @apply text-xs text-gray-500;
   }
   
   .card-footer span {
      @apply mr-3 mt-2 inline-block;
   }
   
   .card-footer strong {
      @apply text-yellow-500 inline-block;
   }
</style>

<script setup>
   
   import { defineEmits } from 'vue'
   
   const emits = defineEmits(['change-tab'])
   
   const changeTab = () => {
      setTimeout(() => {
         emits('changeTab')
      }, 500)
   }
   
   const btnLike = (e) => {
      const clicked = e.target.classList
      if ( clicked.contains('far') ) clicked.replace('far', 'fas')
      else clicked.replace('fas', 'far')
   }
</script>