<template>
   <section class="preview">
      <img :src="currentImg" />
      <i @click="changeTab()" class="fas fa-arrow-left btn-back"></i>
   </section>
   <section class="thumbnails">
      <template v-for="img in images" :key="img" >
         <div @click="changeImg(img)" :class="currentImg === img ? 'active' : ''" class="thumb-box">
            <img :src="img">
         </div>
      </template>
   </section>
</template>

<style>
   
   .preview {
      @apply relative rounded-3xl rounded-t-none overflow-hidden mt-0;
   }
   
   .btn-back {
      @apply text-2xl absolute top-5 left-3 text-gray-50 duration-300;
   }
   
   .btn-back:active {
      transform: scale(1.2);
   }
   
   .thumbnails {
      @apply w-full px-4 mt-5 mb-5 flex overflow-scroll;
   }
   
   .thumb-box {
      @apply rounded-md overflow-hidden border-2 border-gray-100 duration-300;
   }
   
   .active {
      @apply border-yellow-400 shadow-lg;
   }
   
   .thumb-box:not(:last-child) {
      @apply mr-3;
   }
</style>

<script setup>
   
   import { ref, defineEmits } from 'vue'
   
   const images = ref(['house-finder.jpeg', 'house-finder-2.jpg', 'house-finder-3.jpg', 'house-finder-4.jpg', 'house-finder-5.jpeg'])
   const currentImg = ref(images.value[0])
   const emits = defineEmits(['change-tab'])
   
   const changeImg = img => currentImg.value = img
   const changeTab = () => {
      setTimeout(() => {
         emits('change-tab')
      }, 500)
   }
</script>