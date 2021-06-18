<template>
    <h1>wingbling_Acc</h1>
    <ul calss="nav clearfix">
        <li v-for="(item,i) in menu" :key="i">
            <router-link :to="menu[i].link">{{menu[i].title}}</router-link>
        </li>
    </ul>
   
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