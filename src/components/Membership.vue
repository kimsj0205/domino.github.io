<template>
  <div class="membership">
    <div class="inner">
      <div class="text-group" data-aos="fade-up"
      data-aos-duration="1000">
        <h2>도미노 피자에 가입하시고 다양한 혜택을 누리세요!</h2>
        <div class="btn"><router-link>회원가입</router-link></div>
      </div>
      <div class="membership-img">
        <ul>
          <li data-aos="fade-up"
          data-aos-duration="1500" data-aos-delay="300"><img src="../assets/membership1.png" alt="" ></li>
          <li data-aos="fade-up"
          data-aos-duration="1500" data-aos-delay="600"><img src="../assets/membership2.gif" alt="" ></li>
          <li data-aos="fade-up"
          data-aos-duration="1500" data-aos-delay="900"><img src="../assets/membership3.png" alt=""></li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
  .membership{
    width:100%;
    height:450px;
    background:var(--sub-color);
    .inner{
      display:flex;
      justify-content: space-evenly;
      padding-top:100px;
      position:relative;
      &:after{
        content:'';
        width:700px;
        height:2px;
        background:#fff;
        position:absolute;
        bottom:-80px;
        left:50%;
        transform: translateX(-50%);

      }
      .text-group{
        width:350px;
        word-break:keep-all;
        margin-left:30px;
        h2{
          font-weight:700;
          font-size:30px;
          color:#fff;
          line-height:40px;
        }
        .btn{
          margin-top:30px;
        }
      }
      .membership-img{
        ul{
          display:flex;
          gap:30px;
          li{
            box-shadow:2px 2px 5px #0000006b;
            img{
              height:100%;
            }
          }
        }
      }
    }
  }
</style>