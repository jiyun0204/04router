<template>
    <h1>wingbling_Acc</h1>
<!--     
    <ul calss="nav clearfix">
        <li v-for="(item,i) in menu" :key="i">
            <router-link :to="menu[i].link">{{menu[i].title}}</router-link>
        </li>
    </ul>
    -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">wingbling_Acc</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li v-for="(item,i) in menu" :key="i">
            <router-link :to="menu[i].link">{{menu[i].title}}</router-link>
        </li>
    </ul>
  </div>
</nav>
</template>




<script>

export default {
    name:'header',
    data(){
       return{
           menu:[
               {title:'home',link:'/'},
               {title:'product',link:'/product'},
               {title:'board',link:'/board'},
               
           ]
       }
    }
}


</script>




<style>


</style>