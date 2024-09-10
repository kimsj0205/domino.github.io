<template>
  <div class="mainpage">
    <div class="main-text-group">
      <h2>피자는 언제 어디서나<br><strong>도미노 피자!</strong></h2>
      <span>전문가이자 피자 마스터인 한국 도미노피자는 앞으로도 지속적으로 최고의
        피자를 최상의 서비스로 제공하기 위한 노력을 아끼지 않을 것입니다.</span>
      <div class="btn"><router-link>바로가기</router-link></div>
    </div>
    <div class="radius-text">
      <img src="../assets/rotate_text.svg" alt="">
    </div>
    <swiper
      :direction="'vertical'"
      :pagination="{
        clickable: true,
      }"
      :autoplay="{
        delay:3500,
        disableOnInteraction: false,
      }"
      :loop="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide>
        <div class="img-file">
          <img src="../assets/mainslide1.png" alt="">
        </div>
        <div class="text-group">
          <h3>더 가볍게 SON봤다! 매일 한끼 6.900원 부터!</h3>
          <p>해피 데일리 싱글 피자 5종 출시</p>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="img-file">
          <img src="../assets/mainslide2.png" alt="">
        </div>
        <div class="text-group">
          <h3>현대카드 70% M포인트 사용</h3>
          <p>총 금액 70% M포인트 사용 혜택</p>
        </div></swiper-slide>
      <swiper-slide>
        <div class="img-file">
          <img src="../assets/mainslide3.png" alt="">
        </div>
        <div class="text-group white">
          <h3>쏘니 토트넘 홈경기 런던원정대 모집!</h3>
          <p>Team 도미노 파이팅! 피자 주문하고 토트넘 가자!</p>
        </div></swiper-slide>
    </swiper>
  </div>
  
</template>
<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import {Autoplay, Pagination} from 'swiper/modules';

  // Import Swiper styles
  import 'swiper/css';
  import 'swiper/css/pagination';


  // import required modules

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [ Pagination, Autoplay ],
      };
    },
  };
</script>
<style lang="scss">
.mainpage{
  margin-top:140px;
  width:100%;
  height:80vh;
  .swiper{
    width:65% !important;
    height:80% !important;
    margin:0;
    margin-left:auto;
    margin-top:200px;
    img{
      display:block;
      width:100%;
      position: relative;
    }
    .swiper-slide{
      
      height: 100%;
    }
    .text-group{
      width:25em;
      position:absolute;
      bottom:0rem;
      transform: translateY(-40%);
      left:50px;
      width:400px;
      word-break:keep-all;
      color:#303030;
      &.white{
        color:#fff;
        p{
          color:#c9c9c9
        }
      }
      h3{
        font-weight: 500;
        font-size:40px;
      }
      p{
        padding-top:30px;
        color:#9c9c9c
      }
    }
  }
  .swiper-pagination {
    right:30px !important;
  }
  .swiper-pagination-bullet{
    width:10px;
    height:10px;
    margin: 14px 0 !important;
  }
  .swiper-pagination-bullet-active{
    width:10px;
    height:30px;
    border-radius: 5px;
    background-color:var(--sub-color);
  }
}
  .main-text-group{
    position:absolute;
    top:40%;
    width:500px;
    left:10%;
    word-break: keep-all;
    display:flex;
    flex-direction: column;
    gap:30px;
    h2{
      font-size:30px;

      strong{
        font-size:70px;font-weight:700;
      }
    }
    span{
      display:block;
      width:400px;
      color:#9c9c9c;
    }
    img{
      width:300px;
    }
  }
  .radius-text{
    opacity: .3;
    border-radius: 50%;
    width:200px;
    padding-bottom:50px;
    position:absolute;
    bottom:0;
    left:30%;
    img{
      animation: rotate_image 10s linear infinite;transform-origin: 50% 50%;
    }
  }
  
  @keyframes rotate_image{
    100% {
    transform: rotate(360deg);
  }
}
</style>