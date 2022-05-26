<template>
   <div class="col-sm-6 col-md-4 col-lg-3">
       <div class="panel panel-default">
           <div class="panel-body quote">
               <slot></slot>
           </div>
       </div>

   </div>
</template>

<script>
  
</script>

<style> 
    .panel-body {
        font-family: 'Arizania', cursive;
        font-size:20px;
        color: #554f4f;
        background: #ccc;
        text-align: center;
    }

    .quote {
        cursor: pointer;
    }
    .quote:hover {
        background-color: #ffe2e2;
    }
</style>