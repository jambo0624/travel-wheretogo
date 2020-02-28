<template>
  <div class="header">
    <router-link to="/">
      <div class="header-left">
        <div class="iconfont icon-back"></div>
      </div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    overflow hidden
    line-height $headerHeight
    height $headerHeight
    background $bgColor
    color: #fff
    text-align center
    font-size .32rem
    .header-left
      width .64rem
      float left
      .icon-back
        text-align center
        font-size .4rem
        color #fff
</style>
