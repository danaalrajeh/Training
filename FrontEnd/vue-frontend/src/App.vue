<template>
 <div>
   <h1 class="c2">Welcome !!</h1>
   <my-header></my-header>
   <my-footer></my-footer>
   <my-table></my-table>
   <router-view></router-view>
   
 </div>
</template>

<script>
import header from './components/header.vue'
import footer from './components/footer.vue'


  export default {
     components:{
         'my-header':header,
         'my-footer':footer
         
         
         }

     }
  
</script>

<style>
  *{
      box-sizing:border-box;
      margin:0;
  }
  .c2{
    text-align: center;
    color:rgb(214, 25, 129)
  }
</style>