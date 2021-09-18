<template>
   <section class="category">
      <template v-for="item in categoryArr" :key="item">
         <div
            @click="currentCategory = item"
            :class="currentCategory === item ? 'active' : '' " class="category-box">
            {{ item }}
         </div>
      </template>
   </section>
</template>

<style>
   
   .category {
      @apply w-full px-5 py-4 flex overflow-scroll items-center justify-between;
   }
   
   .category-box {
      @apply md:w-4/12 md:mr-5 md:text-center border-gray-300 px-4 py-1 rounded-md duration-300 border;
   }
   
   .active {
      @apply text-gray-50 font-semibold border-gray-50;
   }
   
   .active {
      background: #06B2FD;
   }
</style>

<script setup>
   
   import { reactive, ref } from 'vue'
   
   const categoryArr = reactive(['Apartment', 'Corporate', 'Vilage'])
   const currentCategory = ref('Apartment')
   
</script>