<template>
  <div class="event-page">
    <div class="inner">
      <h2>Event </h2>
      <swiper data-aos="fade-up"
      data-aos-anchor-placement="top-bottom"
      data-aos-duration="1000"
    :slidesPerView="4"
    :space-between="25"
    :pagination="{
      type: 'fraction',
    }"
    :navigation="true"
    :modules="modules"
    :loop="true"
    :loop-additional-slides="1"
    class="mySwiper"
  >
    <swiper-slide>
      <div class="img-box">
        <img src="../assets/eventimg1.jpg" alt="">
        <div class="hover-item">
          <div class="text-box">
            <h3>단체주문 서비스</h3>
            <span>30판 이상 주문도 간편하게</span>
            <div class="btn">
              바로가기
            </div>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="img-box">
        <img src="../assets/eventimg2.jpg" alt="">
        <div class="hover-item">
          <div class="text-box">
            <h3>가맹점 모집</h3>
            <span>도미노피자와 함께하실 가맹점주님들을 모십니다!</span>
            <div class="btn">
              바로가기
            </div>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="img-box">
        <img src="../assets/eventimg3.jpg" alt="">
        <div class="hover-item">
          <div class="text-box">
            <h3>도미노스팟1,324</h3>
            <span>야외에서 피자가 끌릴 땐!</span>
            <div class="btn">
              바로가기
            </div>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="img-box">
        <img src="../assets/eventimg1.jpg" alt="">
        <div class="hover-item">
          <div class="text-box">
            <h3>단체주문 서비스</h3>
            <span>30판 이상 주문도 간편하게</span>
            <div class="btn">
              바로가기
            </div>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="img-box">
        <img src="../assets/eventimg2.jpg" alt="">
        <div class="hover-item">
          <div class="text-box">
            <h3>가맹점 모집</h3>
            <span>도미노피자와 함께하실 가맹점주님들을 모십니다!</span>
            <div class="btn">
              바로가기
            </div>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="img-box">
        <img src="../assets/eventimg3.jpg" alt="">
        <div class="hover-item">
          <div class="text-box">
            <h3>도미노스팟1,324</h3>
            <span>야외에서 피자가 끌릴 땐!</span>
            <div class="btn">
              바로가기
            </div>
          </div>
        </div>
      </div>
    </swiper-slide>
    

  </swiper>
    </div>

  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';


// import required modules
import { Pagination, Navigation } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>
<style lang="scss" scoped>
  .event-page{
    width:100%;
    height:600px;
    background-color:var(--main-color);
    .inner{
      h2{
        font-size:60px;
        color:#fff;
        font-weight: 700;
        text-align:center;
        padding-bottom:60px;
      }
      height:100%;
      .swiper{
        width:100%;
        .swiper-slide{
          border:5px solid #fff;
          box-sizing: border-box;
        }
        .img-box{
          margin:0 auto;
          position:relative;
          overflow: hidden;
          cursor:pointer;
          img{
            width:100%;
            display:block;
          }
          &:hover{
            .hover-item{
              top:0;
            }
          }
          .hover-item{
            transition:.7s ease-out;
            position:absolute;
            width:100%;
            height:100%;
            top:900px;
            left:0;
            background:#000000a8;
            .text-box{
              word-break: keep-all;
              h3{
                font-size:30px;
                text-align:center;
                color:#fff;
                margin-bottom:10px;
                font-weight:700;
              }
              span{
                color:var(--gray-color);
                display:block;
                margin-bottom:20px;
                text-align:center;
              }
              position:absolute;
              top:50%;
              left:50%;
            transform: translate(-50%, -50%);
            }
          }
        }
      }
    }
    
    
  }
  
</style>