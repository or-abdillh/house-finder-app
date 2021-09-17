<template>
   <section class="card">
      <template v-for="card in 5">
         <div class="card-wrapper">
           <div class="card-header">
              <img src="/house-finder.jpeg"/>  
              <i class="fa fa-heart absolute top-3 right-3 text-xl text-gray-500"></i>
           </div> 
           <div class="card-footer">
           <h1 class="text-xl font-medium" >The Penisula Chicago</h1>
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
      @apply w-full mb-5 mx-auto rounded-2xl overflow-hidden border-2 border-gray-200;
   }
   
   .card-header {
      @apply relative;
   }
   
   .card-footer {
      @apply px-5 py-3 bg-gray-100;
   }
   
   .card-footer i {
      @apply text-gray-500;
   }
   
   .card-footer span {
      @apply mr-3 mt-3 inline-block;
   }
   
   .card-footer strong {
      @apply text-yellow-500 inline-block mt-2;
   }
</style>