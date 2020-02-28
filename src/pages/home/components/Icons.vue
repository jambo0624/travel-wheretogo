<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
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
  name: 'home',
  data () {
    return {
      iconList: [
        {
          id: '0001',
          imgUrl: 'https://picbed.qunarzz.com/01d2f57f920666364197a850dab859a8.png',
          desc: '民宿客栈'
        },
        {
          id: '0002',
          imgUrl: 'https://picbed.qunarzz.com/83af731055e121a3251690b225327b56.png',
          desc: '专车自驾'
        },
        {
          id: '0003',
          imgUrl: 'https://picbed.qunarzz.com/5b6737be49ca243072ca614f07803b83.png',
          desc: '信用卡'
        },
        {
          id: '0004',
          imgUrl: 'https://picbed.qunarzz.com/1e107321f5396ea4994cd832232ecf8a.png',
          desc: '旅游团购'
        },
        {
          id: '0005',
          imgUrl: 'https://picbed.qunarzz.com/c65b3bb7571a6bd62df669213e44b84d.png',
          desc: '一日游'
        },
        {
          id: '0006',
          imgUrl: 'https://picbed.qunarzz.com/f6bb08a239ce1b038204120a8d1e4669.png',
          desc: '特惠酒店'
        },
        {
          id: '0007',
          imgUrl: 'https://picbed.qunarzz.com/3a08f360e958ccb2b947049387873ace.png',
          desc: '借钱'
        },
        {
          id: '0008',
          imgUrl: 'https://picbed.qunarzz.com/19b4f6d2fabd617789fa5aad65b249da.png',
          desc: '白金卡'
        },
        {
          id: '0009',
          imgUrl: 'https://picbed.qunarzz.com/799d9d090d1625a854194460c8849fee.png',
          desc: '游轮'
        },
        {
          id: '0010',
          imgUrl: 'https://picbed.qunarzz.com/25e3b9f17a21a6e0113c57a23ffccde4.png',
          desc: '周边短途'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 10)
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
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
  height 0
  padding-bottom 50%
.icon
  overflow hidden
  position relative
  width 20%
  height 0
  float left
  padding-bottom 20%
  .icon-img
    position absolute
    top 10%
    left 10%
    bottom .44rem
    box-sizing border-box
    .icon-img-content
      display block
      margin 0 auto
      height 80%
  .icon-desc
    position absolute
    left 0
    right 0
    bottom 0
    font-size 12px
    line-height .44rem
    height .44rem
    text-align center
    color: $darkTextColor
    ellipsis()
</style>
