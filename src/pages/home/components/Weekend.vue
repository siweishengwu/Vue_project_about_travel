<template>
    <div>
        <div class="recommend-title">
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
                  <button class="item-button">查看详情</button>
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
      imgUrl: `/static/image/r_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    },{
      id: '0002',
      imgUrl: `/static/image/r_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    },{
      id: '0003',
      imgUrl: `/static/image/r_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    },{
      id: '0004',
      imgUrl: `/static/image/r_1.jpg`,
      title: '深圳野生动物园',
      desc: '这里有优雅和呆萌并存的睫毛精'
    }]
  }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
    .recommend-title
      margin-top .2rem
      line-height .8rem
      background #eee
      text-indent .2rem
    .item
      overflow hidden
      display flex
      height 1.9rem
      .item-img
        width 1.7rem
        height 1.7rem
        padding .1rem
      .item-info
        flex 1
        pading .1rem
        min-width 0
        .item-title
          line-height .54rem
          font-size .32rem
          ellipsis()
        .item-desc
          line-height .4rem
          color #ccc
          ellipsis()
        .item-button
          line-height .44rem
          margin-top .16rem
          background #ff9300
          padding 0 .2rem
          border-radius .06rem
          color #fff
</style>


