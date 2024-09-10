<template>
  <div class="menu-list" data-aos="fade-up" data-aos-duration="1500">
    <div class="inner">
    <h3>MENU</h3>
    </div>
    <swiper
    :slidesPerView="4"
    :space-between="30"
    :centeredSlides="true"
    :loopedSlides="5"
    :initial-slide="3"
    :loop="true"
    :loop-additional-slides="1"
    :scrollbar="{
      hide: true,
    }"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide v-for="pizza_item in pizza_item" :key="pizza_item.id" :pizza_item="pizza_item">
      <PizzaItem :pizza_item="pizza_item">
      </PizzaItem>
    </swiper-slide>

  </swiper>
  
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/scrollbar';

// import required modules
import { Scrollbar, Autoplay } from 'swiper/modules';
import PizzaItem from './PizzaItem.vue';

export default {
  data() {
    return{
      pizza_item : [
        {id :1 , title: '클래식 리코타', text: '기본기 강한 토마토 소스에 리코타 치즈로 맛을 더 밀도있게!', price1: 'L: 16,900원', price2 : 'S : 6,900원', src: require('../assets/pizzaimg1.jpg')},
        {id :2 , title: '소시지 맥스', text: '이탈리안 페퍼 소시지, 페퍼로니, 포크, 햄, 불고기까지 5가지 미트를 맥스하게!', price1: 'L : 17,900원', price2 : 'S : 6,900원' , src: require('../assets/pizzaimg2.jpg')},
        {id :3 , title: '포테이토', text: '#도미노피자 No.1 레전드를 8인치 피자로!', price2 : 'S: 7,900원' ,src: require('../assets/pizzaimg3.jpg')},
        {id :4 , title: '블랙타이거 슈림프', text: '#바다와 육지의 대왕 한 판을 8인치 피자로!', price2 : 'S : 11,900원' ,src: require('../assets/pizzaimg4.jpg')},
        {id :5 , title: '치즈 크레이프 샌드', text: '7가지 치즈, 스테이크, 슈림프가 겹겹이 쌓인 맛의 품격!',price1:' L : 34,900원' , price2 : 'M : 29,000원' ,src: require('../assets/pizzaimg5.jpg')},
        {id :6 , title: '블랙타이거 슈림프', text: '7가지 치즈, 스테이크, 슈림프가 겹겹이 쌓인 맛의 품격!',price1:' L : 36,900원' , price2 : 'M : 30,000원' ,src: require('../assets/pizzaimg6.jpg')},
        {id :7 , title: '블록버스터4', text: '#4개 도시의 프리미엄 요리를 품은 블록버스터급 콰트로 피자!',price1:' L : 36,900원' , price2 : 'M : 29,500원' ,src: require('../assets/pizzaimg7.jpg')},
      ]
    }
    
  },
  components: {
    Swiper,
    SwiperSlide,
    PizzaItem
  },
  setup() {
    return {
      modules: [Scrollbar, ],
    };
  },
};
</script>
<style lang="scss" scoped>
  .menu-list{
    margin:30px 0;
    
    .swiper{
      width:100%;
      padding:0 100px; 
      box-sizing: border-box;
    }
    .inner{
      width:800px;
      position:relative;
      h3{
        font-size:70px;
        text-align:center;
        margin-bottom: 100px;
        font-weight:700;
        
      }
      .btn{
        margin: 50px;
        position:absolute;
        right:0px;
    }
    }
    
  }
  
</style>