<template>
  <Membership/>
  <Video/>
  <EventPage/>
</template>
<script>
import EventPage from './EventPage.vue';
import Membership from './Membership.vue';
import Video from './Video.vue';


export default {
  components:{
    Membership,
    Video,
    EventPage
  }
}
</script>
<style lang="scss" scoped>
  
</style>