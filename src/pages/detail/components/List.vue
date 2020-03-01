<template>
  <div class="info">
    <div class="title">{{this.list.title}}</div>
    <div class="price border-bottom"><span class="strong"><i>￥</i>{{this.list.money}}</span><span class="small">起/人</span></div>
    <div class="tag-list border-bottom">
      <span><span>现金红包</span></span>
      <span><span>专享红包</span></span>
      <span><span>代金券</span></span>
      <span><span>优惠促销</span></span>
    </div>
    <div class="tips border-bottom">
      <span><span>早订优惠</span></span>
      <span class="tiny">提前10天预定减20元</span>
    </div>
    <div class="properties">
      <span><span class="iconfont icon-checkin"></span>接送机</span>
      <span><span class="iconfont icon-checkin"></span>出行保障</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .info
    background #fff
    border-radius .2rem .2rem 0 0
    padding .4rem .3rem 0 .3rem
    position relative
    top -0.05rem
    .title
      font-size .36rem
      line-height .51rem
      margin-bottom .1rem
    .price
      padding-bottom .2rem
      .strong
        font-size .44rem
        color #ff8300
        i
          font-size .3rem
      .small
        font-size .24rem
        color #9e9e9e
    .tag-list
      listOneLine()
      span
        border .01rem solid #ff8300
        span
          color #ff8300
    .tips
      listOneLine()
      span
        border .01rem solid #ff1200
        span
          color #ff1200
      .tiny
        border none
        font-size .24rem
        color #616161
    .properties
      padding .21rem 0
      span
        font-size .24rem
        color #616161
        .icon-checkin
          color #1296db
          margin-right .05rem
</style>
