<template>
    <div class="card">
       <div class="card-header">
           <slot name="CardHeader"></slot>
       </div>
   
     <div class="card-body">
       <slot name="CardBody"></slot>
     </div>
   </div>
   </template>
   
   <script>
   export default {
   name: 'CardComp'
   }
   </script>
   
   <style scoped>
   .card{
       width: 18rem;
   }
   
   </style>