<template>
  <div class="footer">
    <div class="inner">
      <h1><img src="../assets/logo.png" alt=""><span class="tel">1577-3082</span></h1>
      <ul class="foot-cont">
        <li><a href="javascript:void(0)">이용약관</a></li>
        <li><a href="javascript:void(0)">개인정보 처리방침</a></li>
        <li><a href="javascript:void(0)">위치기반 서비스</a></li>
        <li><a href="javascript:void(0)">청소년 보호 방침</a></li>
        <li><a href="javascript:void(0)">영상정보처리기기 운영관리방침</a></li>
        <li><a href="javascript:void(0)">고객센터</a></li>
        <li><a href="javascript:void(0)">인재채용</a></li>
        <li><a href="javascript:void(0)">가맹점모집</a></li>
        <li><a href="javascript:void(0)">단체주문</a></li>
      </ul>
      <div class="address">
        <p>06223 서울특별시 강남구 역삼로25길 35(역삼동, 청오큐브타워) 청오디피케이㈜｜대표이사 : 오광현,김영훈</p>
        <p>사업자 등록번호: 220-81-03371｜통신판매업신고: 강남 5064호｜개인정보 보호책임자 : 윤여진｜민원 책임자 : 임영길</p>
        <p>문의 : webmaster@dominos.co.kr</p>
        <small>Copyright ⓒ Domino’s Pizza. All rights reserved.</small>
      </div>
      <ul class="sns">
        <li><a href="javascript:void(0)"><font-awesome-icon :icon="['fab', 'twitter']" size="xl" style="color:#555"/></a></li>
        <li><a href="javascript:void(0)"><font-awesome-icon :icon="['fab', 'facebook-f']" size="xl" style="color:#555"/></a></li>
        <li><a href="javascript:void(0)"><font-awesome-icon :icon="['fab', 'instagram']" size="xl" style="color:#555"/></a></li>
        <li><a href="javascript:void(0)"><font-awesome-icon :icon="['fab', 'youtube']" size="xl" style="color:#555"/></a></li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
  .footer{
    width:100%;
    height:300px;
    
    .inner{
      width:1200px;
      margin:50px auto;
      position:relative;
      
      h1{
      img{
        width:150px;
      }
      .tel{
        font-size:30px;
        font-weight:bold;
        margin-left:20px;
      }
    }
      .foot-cont{
        font-size:18px;
        margin:20px 0;
        display:flex;
        gap:30px;
        color:#7c7c7c;
      }
      .address{
        p{
          font-size:14px;
          color:#7c7c7c;
          line-height:1.5;
        }
        small{
          font-size:14px;
          color:#7c7c7c;
        }
      }
      .sns{
        position:absolute;
        bottom:30px;
        right:30px;
        display:flex;
        gap:10px;
      }
    }
  }
</style>