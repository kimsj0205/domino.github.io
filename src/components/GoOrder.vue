<template>
  <div class="go-order">
    <router-link>
      <p>주문하기</p>
    </router-link>
  </div>
  <div class="go-top" @click="scrollTop">
    <span><font-awesome-icon :icon="['fas', 'angles-up']" style="color:#fff" size="xl"/></span>
  </div>
</template>
<script>
export default {
  methods:{
    scrollTop:function() {
      console.log('확인')
    window.scrollTo({ top: '-140px',  behavior: 'smooth'})
      }
    }
  }

</script>
<style lang="scss" scoped>
  .go-order{
    width:90px;
    height:90px;
    text-align:center;
    line-height:90px;
    color:#fff;
    font-weight: 700;
    border-radius: 50%;
    position:fixed;
    background: var(--sub-color);
    bottom:50px;
    right:50px;
    z-index:999;
    box-shadow:2px 2px 10px #00000059;
    cursor: pointer;
    transition:.2s;
    &:hover{
      background: black;
      color:#fff;
    }
  }
  .go-top{
    width:90px;
    height:90px;
    background:var(--sub-color);
    text-align:center;
    line-height:100px;
    position:fixed;
    bottom:150px;
    border-radius: 50%;
    right:50px;
    z-index:999;
    color:#fff;
    font-weight: 700;
    box-shadow:2px 2px 10px #00000059;
    cursor: pointer;
    transition:.5s;
    &:hover{
      animation: bounce 0.4s 0.1s cubic-bezier(0, 0, 0.18, 0.99) infinite alternate;
      background:var(--main-color);
    }
  }
  @keyframes bounce{
    to{
        transform: translateY(-20px);
    }
}
</style>