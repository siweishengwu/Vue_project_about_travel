<template>
    <div>
        <div class="title">
            周末去哪儿
        </div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
                <div class="item-img-wrapper">
                  <img class="item-img" :src="item.imgUrl" />
                </div>
                <div class="item-info">
                  <p class="item-title">{{item.title}}</p>
                  <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name : 'HomeWeekend',
  data () {
    return {
    recommendList: [{
      id: '0001',
      imgUrl: `/static/image/w_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    },{
      id: '0002',
      imgUrl: `/static/image/w_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    },{
      id: '0003',
      imgUrl: `/static/image/w_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    }]
  }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
    .title
      line-height .8rem
      background #eee
      text-indent .2rem
    .item-img-.item-img-wrapper
      height 0
      overflow hidden
      padding-bottom 33.9%
      .item-img
        width 100%
    .item-info
      padding: .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
</style>


