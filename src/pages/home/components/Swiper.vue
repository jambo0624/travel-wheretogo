<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in list" :key="item.id" v-if="showSwiper">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      }
      // swiperList: [
      //   {
      //     id: '0001',
      //     imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/94/6ca52bb1e782ae6c3c891c7aa1dd2594.water.jpg_600x330_1a1f74b3.jpg'
      //   },
      //   {
      //     id: '0002',
      //     imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/22/3ae746fe7b5a8a9c118c1b4d95897fa8.jpg_600x330_8dbbbf5d.jpg'
      //   },
      //   {
      //     id: '0003',
      //     imgUrl: 'https://img1.qunarzz.com/sight/p0/1505/6d/6d3f80897e1f1eb1.water.jpg_600x330_0ff9d74a.jpg'
      //   },
      //   {
      //     id: '0004',
      //     imgUrl: 'http://img1.qunarzz.com/sight/p0/1901/ed/ed4079d797a78d28a3.water.jpg_600x330_020819e2.jpg'
      //   }
      // ]
    }
  },
  computed: {
    showSwiper() {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
// 样式穿透
.wrapper >>> .swiper-pagination-bullet-active
  background #fff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 55%
  .swiper-img
    width: 100%;

</style>
