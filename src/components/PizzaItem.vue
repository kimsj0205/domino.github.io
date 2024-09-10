<template>
  <div class="under-item">
        <img :src="`${pizza_item.src}`" alt="">
        <div class="hover_item">
          <div class="text-group">
            <h4>{{ pizza_item.title }}</h4>
            <div class="price">
              <p>{{ pizza_item.text}}</p>
              <span>{{ pizza_item.price1}}</span>
              <span>{{ pizza_item.price2}}</span>
            </div>
          </div>
        </div>
      </div>
</template>
<script>
export default {
  props :{
    pizza_item :{
      type: Object,
      required: true,
      default: {}
    }
  }
}
</script>
<style lang="scss" scoped>
  .swiper{
      width:100%;
      .swiper-slide{
        .under-item{
          width:100%;
          height:100%;
          overflow:hidden;
          border-top-left-radius: 50%;
          border-top-right-radius: 50%;
          position:relative;
          margin-bottom:20px;
          &:hover{
            .hover_item
              {
              display:block;
              cursor:pointer
            }
          }
          img{
            width:100%;
            height:100%;
          }
          .hover_item{
            width:100%;
            height:100%;
            color:#fff;
            display:none;
            word-break: keep-all;
            .text-group{
              background-color: #0000009c;
              flex-direction: column;
              justify-content: flex-end;
              display:flex;
              width:100%;
              height: 100%;
              position:absolute;
              left:0;
              top:0;
              h4{
                font-weight: 700;
                font-size:36px;
                text-align:center;
                margin-bottom:30px;
              }
              .price{
                margin:30px 0;
                height:100px;
                p{
                  padding:20px 0;
                  margin-left:30px;
                }
                span{
                  display:block;
                  margin-left:30px;
                }
              }
            }

          }
        }
      }
    }
</style>