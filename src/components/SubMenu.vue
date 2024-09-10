<template>
  <ul class="sub-menu-item">
    <li>
      <router-link>도미노 서비스</router-link>
      <ul>
        <li><router-link>매니아 혜택</router-link></li>
        <li><router-link>도미노 모먼트</router-link></li>
        <li><router-link>퀵오더</router-link></li>
        <li><router-link>단체주문서비스</router-link></li>
      </ul>
    </li>
    <li>
      <router-link >고객센터</router-link>
      <ul>
        <li><router-link>자주하는 질문</router-link></li>
        <li><router-link>문의/칭찬하기</router-link></li>
        <li><router-link>문의 내역/답변</router-link></li>
      </ul>
    </li>
    <li>
      <router-link >회사소개</router-link>
      <ul>
        <li><router-link>한국도미노피자</router-link></li>
        <li><router-link>광고갤러리</router-link></li>
        <li><router-link>사회공헌활동</router-link></li>
        <li><router-link>가맹점 모집</router-link></li>
        <li><router-link>인재채용</router-link></li>
      </ul>
    </li>
    <li>
      <router-link >공지사항</router-link>
      <ul>
        <li><router-link>도미노 뉴스</router-link></li>
        <li><router-link>보도자료</router-link></li>
      </ul>
    </li>
  </ul>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
  .sub-menu-item{
    display:flex;
    width:100%;
    padding:20px;
    box-sizing:border-box;
    >li{
      width:calc(100% / 4);
      font-size:16px;
      font-weight: 600;
      >router-link{
        border-bottom:1px solid var(--gray-color);
        display:block;
        margin-right:40px;
        padding-bottom:10px;
      }
      ul{
        color:#757575;
        padding-top:10px;
        font-weight: 400;
        li{
          cursor: pointer;
          width:100%;
          padding:8px 0;
        }
      }
    }
  }
</style>