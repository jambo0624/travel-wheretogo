<template>
  <div class="container">
    <div v-for="tip in tips" :key="tip.id">
      <div class="title border-bottom">
        <span>{{tip.title}}</span>
      </div>
      <h3 class="subtitle">{{tip.subtitle}}</h3>
      <div>
        <div v-for="item in tip.items" :key="item.id" class="item">
          {{item.item}}<br>
          <div v-if="item.details.length > 0" v-for="(detail, index) in item.details" :key="index">{{detail}}<br></div>
          <div v-else>{{item.details}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'DetailDeclare',
  props: {
    tips: Array
  }
}
</script>

<style lang="stylus" scoped>
  .container
    background #fff
    margin-top .2rem
    padding .2rem .3rem
    .title
      padding .2rem .2rem
      line-height .3rem
      height .3rem
      span
        font-size .3rem
        color #00bcd4
        font-weight bold
    .subtitle
      padding: .5rem .1rem .3rem;
      margin: 0 auto;
      font-size: 18px;
      text-align: center;
      font-weight: 400;
      background-color: #fff;
      color: #212121;
    .item
      line-height .5rem
</style>
