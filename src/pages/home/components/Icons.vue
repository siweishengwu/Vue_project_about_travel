<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data () {
    return {
      iconList: [
        {
          id: "0001",
          imgUrl:
            `/static/image/i_1.png`,
          desc: "景点门票"
        },
        {
          id: "0002",
          imgUrl:
            `/static/image/i_2.png`,
          desc: "广州必游"
        },
        {
          id: "0003",
          imgUrl:
            `/static/image/i_3.png`,
          desc: "动植物园"
        },
        {
          id: "0004",
          imgUrl:
            `/static/image/i_4.png`,
          desc: "自然风光"
        },
        {
          id: "0005",
          imgUrl:
            `/static/image/i_5.png`,
          desc: "珠江夜游"
        },
        {
          id: "0006",
          imgUrl:
            `/static/image/i_6.png`,
          desc: "泡温泉"
        },
        {
          id: "0007",
          imgUrl:
            `/static/image/i_7.png`,
          desc: "一日游"
        },
        {
          id: "0008",
          imgUrl:
            `/static/image/i_8.png`,
          desc: "长隆度假区"
        },
        {
          id: "0009",
          imgUrl:
            `/static/image/i_9.png`,
          desc: "广州塔"
        }]
    }
  },
  computed: {
    pages() {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
@import '~styles/varibles.styl';

.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
}
.icons
  margin-top .1rem
  .icon {
    position: relative;
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding: 0.1rem;

      .icon-img-content {
        display: block;
        margin: 0 auto;
        height: 100%;
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      color: $darkTextColor;
      text-align: center;
      overflow: hidden;
      white-space nonerap
      ellipsis()
  }
}
</style>

