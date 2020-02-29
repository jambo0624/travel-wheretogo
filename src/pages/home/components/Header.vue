<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont icon-back"></div>
    </div>
    <input class="header-input" placeholder="输入城市/景点/游玩主题" type="text" />
    <span class="iconfont icon-search"></span>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont icon-arrow"></span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  // 1rem = html font-size = 50px
  // 左右定宽，中间flex:1 是经典的三栏布局
  @import '~styles/varibles.styl'
  .header
    display flex
    line-height $headerHeight
    background $bgColor
    color: #fff
    .header-left
      width .64rem
      float left
      .icon-back
        text-align center
        font-size .4rem
    .header-input
      flex 1
      background #fff
      box-sizing border-box
      border-radius .1rem
      margin-top .12rem
      line-height .64rem
      padding-left .55rem
      height .64rem
      margin-left .2rem
      color #ccc
      position relative
    .header-input:focus::placeholder
      color: transparent
    .icon-search
      position absolute
      left 1rem
      color #ddd
    .header-right
      min-width 1.04rem
      padding 0 .1rem
      float right
      text-align center
      color #fff
</style>
