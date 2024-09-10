<template>
  <div class="brandstory">
    <div class="img" data-aos="fade-up" data-aos-duration="1000">

    </div>
    <div class="text-group" data-aos="fade-up" data-aos-duration="2500">
      <h3>BRANDSTORY</h3>
      <span>전문가이자 피자 마스터인 한국 도미노피자는 앞으로도 지속적으로 최고의
        피자를 최상의 서비스로 제공하기 위한 노력을 아끼지 않을 것입니다.</span>
      <div class="btn">바로가기</div>
    </div>
  </div>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
  .brandstory{
    margin:200px 0;
    display:flex;
    .img{
      background: url(../assets/brandimg.jpg) no-repeat center/cover;
      width:60%;
      height:600px;
    }
    .text-group{
      width:500px;
      padding:150px 50px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      gap:40px;
      word-break: keep-all;
      h3{
        font-size:60px;
        font-weight:700;
      }
      span{
        color:#9c9c9c;
      }
    }
  }
</style>