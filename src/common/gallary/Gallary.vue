<template>
  <div class="container" @click="handleGarraryClick">
    <div class="wrapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="item in imgs" :key="item.id">
          <img class="gallary-img" :src="item.imgUrl" />
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Gallary',
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        loop: true,
        observeParents: true,
        observer: true
      }
    }
  },
  props: {
    imgs: {
      type: Array,
      default() {
        return [
          {
            id: '0001',
            imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/ fafe9394-8e5f-4ca9-b284-0cde9e516723.jpg_r_1280x840x95_cd6f7120.jpg'
          },
          {
            id: '0002',
            imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/ 9ef888c0-5965-446b-9a8f-63d1e92f45b1.jpg_r_1280x840x95_cb14b111.jpg'
          },
          {
            id: '0003',
            imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/ abfe690d-a57c-4dd3-8e77-f1b0e396775d.jpg_r_1280x840x95_dbc77d7b.jpg'
          }
        ]
      }
    }
  },
  methods: {
    handleGarraryClick() {
      this.$emit('close')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow inherit
  .container
    display flex
    flex-direction column
    justify-content center
    z-index 99
    position fixed
    left 0
    right 0
    top 0
    bottom 0
    background #000
    .wrapper
      background #fff
      .gallary-img
        width 100%
    .swiper-pagination
      color #fff
      bottom -1rem
</style>
