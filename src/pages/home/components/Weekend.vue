<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
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
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/e2/e29a46fda7841796a3.img.jpg_600x330_05a3ccd5.jpg',
          title: '大阳古镇',
          desc: '小编为您精挑细选，性价比硬货！'
        },
        {
          id: '0002',
          imgUrl: 'https://img1.qunarzz.com/sight/p0/1412/40/a04663db73109dda14b3fd6bc84aae3f.water.jpg_600x330_be6780c0.jpg',
          title: '恒山(AAAA景区)',
          desc: '恒山手机自动导游14个讲解，不含门票'
        },
        {
          id: '0003',
          imgUrl: 'https://img1.qunarzz.com/sight/p0/1505/4a/4a6a13b556fae3db.water.jpg_600x330_f86f48c6.jpg',
          title: '大同华严寺(AAAA景区)',
          desc: '华严寺景区手机电子语音讲解，含22个景点讲解'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  line-height .8rem
  margin-top .2rem
  background #eee
  text-indent .2rem
.item-img-wrapper
  overflow hidden
  height 0
  padding-bottom 55%
  .item-img
    width 100%
.item-info
  padding .1rem
  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
  .item-desc
    line-height .4rem
    color #ccc
    ellipsis()
</style>
