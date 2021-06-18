<template>
     <swiper :pagination="true" class="mySwiper mb-5">
  <swiper-slide><img src="/image/slide01.jpg" alt=""></swiper-slide>
  <swiper-slide><img src="/image/slide02.jpg" alt=""></swiper-slide>
  </swiper>
  <div class="jully">
    <div class="container">
      <h2>jully product</h2>
       <p>Lorem ipsum dolor sit amet consectetur.</p>
       <div class="row mb-5">
        <div class="col-sm-6 col-md-3" v-for="(item,i) in 8" :key="i">
        <img :src="pdata[i].image" alt="" class="w-100">
        <div @click="$emit('pOpen',pdata[i].id)">{{pdata[i].title}}</div>
        </div>
      </div>

      <div class="btn btn-primary m-auto d-block" style="width:100px">
     <router-link to="/product">more</router-link>
     </div>
    </div>
    </div>

</template>
 
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import "swiper/components/pagination/pagination.min.css"
import 'swiper/swiper.scss';

// import Swiper core and required modules
import SwiperCore, {
  Pagination
} from 'swiper/core';

// install Swiper modules
SwiperCore.use([Pagination]);

export default{
  props:['pdata'],
  components: {
    Swiper,
    SwiperSlide,
  },
}



</script>

<style>
*{margin: 0;padding: 0; box-sizing:border-box;}
li{list-style: none;}
a{text-decoration: none; display:block;}
a:link, a:visited{color:gray}
.clearfix:after{content:""; display: block; clear:both;}
.title li {float: left; width:calc( 100% /3); text-align:center;line-height: 50px;}
h1{text-align: center; margin-bottom: 20px;}
.title li:hover{background:skyblue;}
.footer {padding:20px; background:#ccc;}

.swiper-container {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.jully h2{text-align: center;}
.jully h2:after{content:"";width: 30px;height: 1px;background: #333; display: block;margin:10px ;}
.jully p{text-align: center;}
</style>