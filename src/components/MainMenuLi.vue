<template>
  <ul class="menu">
    <li v-for="mainMenu in mainMenu" :key="mainMenu">
      <router-link>{{ mainMenu }}</router-link>
    </li>
  </ul>

</template>
<script>
export default {
  props:{
    mainMenu: Object,
    default : ''
  }
}
</script>
<style lang="scss" scoped>
  ul.menu{
    width:800px;
    height:50px;
    align-items: center;
    display:flex;
    justify-content: flex-end;
    justify-content: space-evenly;
    li{
      width: calc(100% / 6);
      text-align:center;
      height:100%;
      line-height:50px;
      box-sizing:border-box;
      &:hover{
        border-bottom:2px solid red;
        font-weight: 700;
        cursor: pointer;
      }
      a{
        display:block;
      }
    }
  }
</style>