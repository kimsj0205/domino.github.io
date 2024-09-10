<template>
  <Header :scrollDirection="scrollDirection"/>
  <MainContainer/>
  <Footer/>
  <GoOrder/>
</template>

<script>
import { ref, onMounted } from 'vue';
import GoOrder from './components/GoOrder.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import MainContainer from './components/MainContainer.vue';
  import './scss/common.scss';
  import './scss/font.css';

export default {
  name: 'App',
  components: {
    Header,
    MainContainer,
    Footer,
    GoOrder
  },
  setup(){
    const scrollDirection = ref(0); // 1: up, -1 : down
    // Throttle을 위한 ref
    const waiting = ref(false);
    // 이전 스크롤 방향을 저장하기 위한 ref
    const scrollTrace = ref(0);
// Throttle이 적용된 이벤트 핸들러
    function scrollHandler(e){
      if(!waiting.value){
        waiting.value = true; // throttle check
        const currentScroll = window.scrollY; // current scrollY
        if(currentScroll > scrollTrace.value) scrollDirection.value = -1;
        else if(currentScroll < scrollTrace.value) scrollDirection.value = 1;
        scrollTrace.value = currentScroll;
        // Event Throttle 100 ms
        setTimeout(()=>{
          waiting.value = false;
        }, 100); 
            }
          }
          onMounted(()=>{
          // DOM이 마운트 되었을 때 이벤트 핸들러를 등록한다.
            document.addEventListener('scroll',scrollHandler);
        });
      return {
      scrollDirection
    }
  }
}


</script>

<style>

</style>
