<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="https://img1.qunarzz.com/vs_ceph_vs_tts/fafe9394-8e5f-4ca9-b284-0cde9e516723.jpg_r_640x420x95_f5bdfb68.jpg">
      <div class="banner-info">
        <div class="banner-title">产品编号 3174821387</div>
        <div class="banner-number">
          1/6 <span class="iconfont icon-image"></span>
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGarrary" @close="handleGarraryClick"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'Banner',
  data() {
    return {
      showGarrary: false,
      imgs: [
        {
          id: '0001',
          imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/fafe9394-8e5f-4ca9-b284-0cde9e516723.jpg_r_1280x840x95_cd6f7120.jpg'
        },
        {
          id: '0002',
          imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/9ef888c0-5965-446b-9a8f-63d1e92f45b1.jpg_r_1280x840x95_cb14b111.jpg'
        },
        {
          id: '0003',
          imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/abfe690d-a57c-4dd3-8e77-f1b0e396775d.jpg_r_1280x840x95_dbc77d7b.jpg'
        }
      ]
    }
  },
  methods: {
    handleBannerClick() {
      this.showGarrary = true
    },
    handleGarraryClick() {
      this.showGarrary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position relative
  overflow hidden
  height 0
  padding-bottom 55%
  .banner-img
    width 100%
  .banner-info
    position absolute
    left 0
    right 0
    bottom 0
    line-height .6rem
    display flex
    color #fff
    .banner-title
      flex 1
      font-size .32rem
      padding 0 .2rem
    .banner-number
      height .4rem
      line-height .4rem
      margin-top .1rem
      padding 0 .4rem
      border-radius .2rem
      background rgba(0, 0, 0, 0.8)
      font-size .24rem
      .icon-image
        font-size .24rem
</style>
