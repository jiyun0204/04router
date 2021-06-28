<template>

    <div v-if="pView==true">
        <div class="pPop text-center">
            <img v-bind:src="pdata[pNum].image" alt="" class="w-100">
            <p>{{pdata[pNum].title}}</p>
            <button class="btn btn-primary" @click="pView=false">닫기</button>
        </div>
    </div>


    <theader />
    <router-view
    :pdata="pdata"
    @pOpen="pView=true;pNum=$event"
    
    >
    </router-view>
</template>

<script>
import header from './components/haeder.vue'
import pdata from './pdata.js'



export default {
    name:'app',
    components:{
    'theader':header,
    },
    data(){
        return{
            pdata:pdata,
            pView:false,
            pNum:0
        }
    }
}
</script>

<style>
*{margin: 0;padding:0;}
  a:link,a:visited{
    text-decoration: none;color:#333;
  }

  li{list-style: none;}
  .clearfix:after{content:"";display: block;clear:both}



  h1{text-align: center;margin-bottom:10px;}
  .nav{
    border-top:1px solid #ddd;border-bottom:1px solid #ddd
    }
  .nav li{float:left;width:calc(100% / 3);text-align:center;line-height:40px;}

  .pPop{position:fixed; z-index:10; background: #ccc; width: 80%; 
  top:50%;left:50%; transform:translate(-50%,-50%); box-shadow:0 0 10px rgba(0,0,0,0.5);
  border-radius:10px;padding:20px;}

.pView{background:#fff;width:70%;position: fixed;top:50%;left:50%;transform:translate(-50%,-50%);
    z-index:10;box-shadow:0 0 10px rgba(0,0,0,0.5);padding:20px;border-radius:10px
  }

.fade-enter-from{opacity: 0;}
.fade-enter-active{transition: 0.5s;}
.fade-enter-to{opacity: 1;}


.fade-enter-from{opacity: 1;}
.fade-enter-active{transition: 0.3s;}
.fade-enter-to{opacity: 0.5;}


  @media screen and (min-width:900px){
      .pPop{width:800px;}

  }
</style>

