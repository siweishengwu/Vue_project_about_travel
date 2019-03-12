<template>
<div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"><img>
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
            },
            swiperList:[{
                id:'0001',
                imgUrl:`/static/image/1.jpg`
            },{
                id:'0002',
                imgUrl:`/static/image/2.jpg`,
            }]
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


