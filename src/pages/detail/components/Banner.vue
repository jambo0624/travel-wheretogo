<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg">
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number">
          1/{{this.bannerImgs.length}} <span class="iconfont icon-image"></span>
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallary :imgs="bannerImgs" v-show="showGarrary" @close="handleGarraryClick"></common-gallary>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'Banner',
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
  },
  data() {
    return {
      showGarrary: false
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
    CommonGallary,
    FadeAnimation
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position relative
  overflow hidden
  height 0
  padding-bottom 65%
  .banner-img
    width 100%
  .banner-info
    position absolute
    left 0
    right 0
    bottom 0.1rem
    line-height .6rem
    display flex
    color #fff
    .banner-title
      flex 1
      font-size .28rem
      padding 0 .3rem
    .banner-number
      height .4rem
      line-height .4rem
      margin-top .1rem
      padding 0 .2rem
      font-size .24rem
      .icon-image
        font-size .24rem
</style>
