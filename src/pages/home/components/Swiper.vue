<template>
<div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide>
        <img class="swiper-img" src="~@/assets/image/1.jpg"><img>
    </swiper-slide>
    <swiper-slide>
         <img class="swiper-img" src="~@/assets/image/2.jpg"><img>
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination">
    </div>
    </swiper>
</div>
</template>
<script>
export default {
    name: 'HomeSwiper',
    data () {
        return{
            swiperOption:{
                pagination: '.swiper-pagination',
                loop: true
            }
        }
    }
}
</script>
<style lang="stylus">
    .wrapper
      width 100%
      height 0
      overflow hidden
      padding-bottom:26.7%
      background #eee
      .swiper-pagination swiper-pagination-bullets
        background red !improtant
      .swiper-img
        width 100%

</style>


