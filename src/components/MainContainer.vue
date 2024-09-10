<template>
  <div class="main-container">
    <MainSlide/>
    <MenuList/>
    <BrandStory/>
    <Section/>
  </div>
</template>
<script>

import BrandStory from './BrandStory.vue';
import MainSlide from './MainSlide.vue';
import MenuList from './MenuList.vue';
import Section from './Section.vue';


export default {
  components : {
    MainSlide,
    MenuList,
    BrandStory,
    Section
  }
}
</script>
<style lang="scoped">
  
</style>