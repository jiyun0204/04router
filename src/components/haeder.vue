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
<table class="table">
  <thead>
    <tr>
      <th scope="col">No.</th>
      <th scope="col">고객이름</th>
      <th scope="col">상품명</th>
      <th scope="col">수신확인</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>미확인</td>
      <td>확인</td>
      <td>미확인</td>
    </tr>
  </tbody>
</table>
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