<template>
   <section class="navbar">
      <div class="menu-box">
         <i class="fas fa-bars duration-300"></i>
      </div>
      <div class="menu-box bg-gray-300 px-2 py-1 rounded-md">
         <i class="fas fa-user duration-300"></i>
      </div>
      <div class="greetings">
         <h1>Find Your Dream <br /> Home</h1>
      </div>
   </section>
</template>

<style >
   
   .navbar {
      @apply w-full px-5 py-4 flex flex-wrap items-center justify-between;
   }
   
   .menu-box {
      @apply text-gray-700 text-2xl;
   }
   
   .menu-box i:active { 
      transform: scale(.75);
   }
   
   .greetings {
      @apply w-full font-medium text-gray-700 text-3xl mt-5;
   }
</style>