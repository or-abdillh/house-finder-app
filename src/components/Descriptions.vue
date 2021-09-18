<template>
   <section class="descriptions">
      <div class="header">
         <div>
            <h1 class="font-bold" >The Peninsula Chicago</h1>
            <span>
               <template v-for="star in 5">
                  <i class="text-yellow-500 fa fa-star" ></i>
               </template>
               <small class="ml-2">8.9</small>
            </span>
         </div>
         <div>
            <strong>$1500</strong>
            <br />
            <small class="text-gray-400">/month</small>
         </div>
      </div>   
      <div class="footer">
         <template v-for="(thumb, index) in thumbs" :key="index" >
            <div class="thumb-wrapper">
               <div class="icon-wrapper" :class="thumb.bg">
                  <i :class="thumb.icons" ></i>
               </div>
               <small class="text-xs font-semibold">{{ thumb.text }}</small>
            </div>
         </template>
      </div>   
   </section>
</template>

<style>
   
   .descriptions {
      @apply px-4;
   }
   
   .descriptions .header {
      @apply flex justify-between mb-5;
   }
   
   .footer {
      @apply flex justify-between mt-10;
   }
   
   .footer .thumb-wrapper {
      @apply w-3/12 text-center;
   }
   
   .footer .thumb-wrapper:not(:last-child) {
      @apply mr-5;
   }
   
   .footer .thumb-wrapper .icon-wrapper {
      @apply text-center py-3 mb-2 rounded-md border-2 border-gray-200;
   }
   
   .thumb-primary {
      color: #2BB8E4;
   }
   
   .thumb-secondary {
      color: #322ECB;
   }
   
   .thumb-bg-primary {
      background: #E0F9FD;
   }
   
   .thumb-bg-secondary {
      background: #E4E5FC;
   }
   
</style>

<script setup>
   
   import { reactive } from 'vue'
   
   const thumbs = reactive([
         {
            icons: 'fa fa-bed thumb-secondary',
            text: '4 bedrooms',
            bg: 'thumb-bg-primary'
         },
         {
            icons: 'fas fa-sink thumb-primary',
            text: '2 washroom',
            bg: 'thumb-bg-primary'
         },
         {
            icons: 'fa fa-bath thumb-secondary',
            text: '1 kitchen',
            bg: 'thumb-bg-secondary'
         },
         {
            icons: 'fas fa-person-booth thumb-secondary',
            text: '1 drawing',
            bg: 'thumb-bg-secondary'
         }
      ])
   
</script>