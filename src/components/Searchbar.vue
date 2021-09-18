<template>
   <section class="search-bar">
      <div class="search-wrapper">
         <span class="text-gray-600">
            <i class="fa fa-search"></i>
         </span>
         <input type="text" placeholder="Search"/>
      </div>
      <button class="btn-filter" type="button">
         <i class="fas fa-filter duration-300"></i>
      </button>
   </section>   
</template>

<style>
   
   .search-bar {
      @apply w-full px-5 flex items-center justify-between;
   }
   
   .search-wrapper {
      @apply px-3 py-3 overflow-hidden flex justify-between w-10/12 rounded-xl;
   }
   
   .search-wrapper input {
      @apply w-full px-3 focus:placeholder-gray-700;
   }
   
   
   input[type=text]:focus, input[type=text]:active {
      outline: none;
   }
   
   .search-wrapper, .search-wrapper input, .search-wrapper i {
      background: #FAFAFA;
   }
   
   .btn-filter {
      @apply px-3 py-2 text-xl rounded-md text-gray-50;
   }
   
   .btn-filter i:active {
      transform: scale(.75);
   }
   
   .btn-filter {
      background: #06B2FD;
   }
</style>