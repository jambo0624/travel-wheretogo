<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont icon-back"></div>
    </div>
    <div class="header-input">
      <span class="iconfont icon-search"></span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont icon-arrow"></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  // 1rem = html font-size = 50px
  // 左右定宽，中间flex:1 是经典的三栏布局
  @import '~styles/varibles.styl'
  .header
    display flex
    line-height .86rem
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
      border-radius .1rem
      margin-top .12rem
      line-height .64rem
      padding-left .2rem
      height .64rem
      margin-left .2rem
      color #ccc
    .header-right
      width 1.24rem
      float right
      text-align center
</style>
