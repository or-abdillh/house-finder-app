<template>
   <section class="actions">
      <button class="btn-call" type="text">Call</button>
      <button class="btn-msg" type="text">Message</button>
   </section>
</template>

<style>
   
   .actions {
      @apply mt-5 mb-3 px-4 flex justify-between text-center;
   }
   
   .btn-call, .btn-msg {
      @apply border-2 border-gray-200 rounded-md px-4 py-2 font-medium;
   }
   
   .btn-msg {
      @apply w-7/12 text-gray-50;
   }
   
   .btn-msg {
      background: #06B2FD;
   }
   
   .btn-call {
      @apply w-4/12 text-gray-700;
   }
</style>