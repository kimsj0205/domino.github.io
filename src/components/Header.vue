<template>
  <div class="header" :class="headerShownClass">
    <div class="inner">
      <h1><img src="../assets/logo.png" alt=""></h1>
      <div class="top-menu">
        <ul>
          <li><router-link>로그인</router-link></li>
          <li><router-link>회원가입</router-link></li>
          <li>
            <select name="language" id="lang">
              <option value="KO">KOR</option>
              <option value="ENG">ENG</option>
            </select>
          </li>
        </ul>
      </div>
      <div class="main-menu">
          <MainMenuLi :mainMenu="mainMenu"/>
          <button @click="eventActive">+</button>
      </div>
    </div>
    <div class="sub-menu" :class="{active : isActiveA}">
      <transition name="fade">
        <div class="inner" v-if="show">
          <SubMenu/>
        </div>
      </transition>
    </div>
  </div>
</template>
<script>
import { computed } from 'vue';
import MainMenuLi from './MainMenuLi.vue';
import SubMenu from './SubMenu.vue';


export default {
  data() {
    return {
      mainMenu : ['메뉴', 'e-쿠폰','상품권 선물', '이벤트 제휴', '매장 검색', '가맹점 모집'],
      isActiveA : false,
      show:true
    }
  },
  props:{
      scrollDirection:Number,
  },
  setup(props){
    const headerShownClass=computed(()=>{
    if(props.scrollDirection === -1) return 'header_off';
      return '';	
      });
	    return {
        headerShownClass 
    }
  },
  methods :{
    eventActive(){
      this.isActiveA = !this.isActiveA;
    }
  },
  components:{
    MainMenuLi,
    SubMenu
  }
}
</script>
<style lang="scss" scoped>
  .header{
    position:fixed;
    top:0;
    left:0;
    z-index:100;
    background-color:#fff;
    width:100%;
    height:140px;
    border-bottom:1px solid var(--gray-color);
    .inner{
      display: flex;
      position:relative;
      h1{
      width:200px;
      height: 140px;
      img{
        margin:40px 0;
        width:100%;
      }
      }
      .main-menu{
        position:absolute;
        margin-right:200px;
        bottom:10px;
        right:0;
        button{
          position:absolute;
          bottom:25px;
          right:-40px;
          width: 30px;
          height:30px;
          border:none;
          background: inherit;
          font-size:50px;
          cursor:pointer;
        }
      }
      .top-menu{
        height:30px;
        margin-right:150px;
        margin-left: auto;
        margin-top:10px;
        ul{
          display:flex;
          gap:30px;
          li{
            color: #444;
            line-height:30px;
            font-size:14px;
            select{
              border-radius: 20px;
              padding: 0.3em; margin: 0;
              &:hover {
              border-color: #888;
              }
              &:focus {
                border-color: #aaa;
                box-shadow: 0 0 1px 1px rgba(59, 153, 252, 0.7);
                box-shadow: 0 0 0 3px -moz-mac-focusring;
                color: #222;
                outline: none;
              }
              &:disabled {
                opacity: 0.5;
              }
            }
          }
        }
      }
    }

    .sub-menu{
      z-index:10;
      background-color:#fff;
      position:absolute;
      left:0;
      width:100%;
      height:0;
      top:140px;
      
      transition:.4s;
      overflow:hidden;
      &.active{
        display: block;

        left:0;
        height: 250px;
      }
    }
  }
  .header_off{
    top:0;
    left:0;
    background-color:#fff;
    width:100%;
    height:70px;
    .inner{
      h1{
        height: 70px;
        display:flex;
        align-items: center;
        img{
          margin:0;
        }
      }
    }
    .sub-menu{
      top:70px;
    }
    .top-menu{
      display:none;
    }
  }
</style>