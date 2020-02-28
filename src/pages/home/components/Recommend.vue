<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'https://m.tuniucdn.com/filebroker/cdn/online/5b/f7/5bf708b7_w80_h80_c1_t0.jpg',
          title: '「双人价格套餐-穿越宋朝-宋城自驾2日游」宿宋城千古情主题酒店（西湖店）游宋城，自选单人套餐/双人套餐/三人套餐，赏千古情贵宾席表演',
          desc: '穿越宋朝 主题乐园 宋代cos秀'
        },
        {
          id: '0002',
          imgUrl: 'https://m.tuniucdn.com/fb2/t1/G2/M00/1A/22/Cii-T1gz0jqIQUaAAI4afc21-FAAAErZQDif9sAjhqV720_w80_h80_c1_t0.JPG',
          title: '「大年初一风景小镇2-4日自驾游」自选行程//温泉套餐，网红度假村，另可加购藏龙百瀑/中国大竹海/竹博园/凯蒂乐园等景区门票',
          desc: '大年初一 风景小镇'
        },
        {
          id: '0003',
          imgUrl: 'https://m.tuniucdn.com/fb2/t1/G2/M00/59/08/Cii-T1jXXC-IewyVAB_atPIGQbQAAIy2AC-TD4AH9rM332_w80_h80_c1_t0.jpg',
          title: '「宋城千古情主题酒店西湖店2-3日自驾游」双人/三人/两大一小/两大两小套餐任选  游宋城 观千古情演出（贵宾席）',
          desc: '主题酒店 自驾游 演出'
        },
        {
          id: '0004',
          imgUrl: 'https://m.tuniucdn.com/fb2/t1/G5/M00/08/B9/Cii-slsCcKCIXMw8AH_AimZIfeIAAHIeAKauikAf8Ci957_w80_h80_c1_t0.jpg',
          title: '「绿城度假酒店2-4日自驾游」可加订中心湖区/森林氧吧/千岛秘境等景区门票',
          desc: '绿城度假  天然氧吧'
        },
        {
          id: '0005',
          imgUrl: 'https://m.tuniucdn.com/fb2/t1/G5/M00/78/99/Cii-tFqWXsSIX0a-AARmLOJde2oAADvkwOj5jQABGZE891_w80_h80_c1_t0.jpg',
          title: '「自驾2日游」宿ClubMedJoyview安吉度假村，体验一个多元文化的特别假期',
          desc: '远离市井喧嚣 欣赏自然秀丽  感受竹海翠绿'
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
.item
  height 1.9rem
  display flex
  overflow hidden
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-button
      margin-top 0.3rem
      background #ff9300
      padding 0 .1rem
      border-radius .06rem
</style>
