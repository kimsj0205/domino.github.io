<template>
  <div class="youtube-video">
    <div class="inner">
      <h3>Video</h3>
      <div id="player">
        <!-- props 넣을 때 쿼리문으로 -->
        <iframe
          :width="1200"
          :height="600"
          style="border-radius: 20px; box-shadow:2px 2px 5px #0606063d"
          :src="`https://www.youtube.com/embed/${state.videoId}?autoplay=1&mute=1&controls=0&loop=1&playlist=WqNBIkFOoE4`"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture;"
          allowfullscreen
        />
      </div>
  

    </div>
  </div>
</template>
<script>
import { defineComponent, reactive } from "vue";

export default defineComponent({
  data(){
    return{
    }
  },
  setup() {
    const state = reactive({
      videoId: 'WqNBIkFOoE4',
    });
    return {
      state,
    };
  },
});

</script>
<style lang="scss" scoped>
  .youtube-video{
    width:100%;
    height:800px;
    background: linear-gradient(var(--sub-color)20%,#fff 5% 70%, var(--main-color)15%);
    .inner{
      margin:0 auto;
      #player{
        margin:50px auto;
        width:1200px;
      }
      h3{
        font-size:60px;
        color:#fff;
        font-weight: 700;
        text-align:center;
      }
    }
  }
</style>