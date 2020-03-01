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
  name: 'Declare',
  data() {
    return {
      tips: [
        {
          id: '0001',
          title: '特殊说明',
          subtitle: '费用不含',
          items: [
            {
              id: '0001',
              item: '【不可抗力】',
              details: ['因交通延阻、罢工、天气、飞机、机器故障、航班取消或更改时间等不可抗力原因所导致的额外费用']
            },
            {
              id: '0002',
              item: '【个人消费】',
              details: ['1、酒店内洗衣、理发、电话、传真、收费电视、饮品、烟酒等个人消费', '2、购物等个人消费以及因个人疏忽、违章或违法引起的经济损失或赔偿费用', '3、当地参加的自费项目以及 “费用包含”中不包含的其它项目']
            },
            {
              id: '0003',
              item: '【单房差】',
              details: ['1、单房差', '2、升级舱位、升级酒店、升级房型等产品的差价']
            },
            {
              id: '0004',
              item: '【餐饮】',
              details: ['散客行程不含餐费，请自愿跟导游自理团餐或自备干粮']
            },
            {
              id: '0005',
              item: '【儿童】',
              details: ['儿童不占床，如需占床请补交费用']
            }
          ]
        },
        {
          id: '0002',
          title: '',
          subtitle: '儿童说明',
          items: [
            {
              id: '0001',
              item: '1、儿童费用包含行程中车位费，不含早餐，不占床位，不含机票',
              details: ['价格：￥630起/人', '价格说明：儿童套餐费用只含车费，不含赠送项目和住宿，如有产生则自理。因儿童机票情况有点特殊，所以此费用是不含儿童机票，机票根据游客出行时间具体核价，看按成人价出票，还是购买儿童票划算，请致电详询供应商。']
            }
          ]
        },
        {
          id: '0003',
          title: '',
          subtitle: '老人说明',
          items: [
            {
              id: '0001',
              item: '1、60周岁（含）以上老年人预订出游，须有家属或朋友陪同方可出游; 因服务能力所限，不接受70周岁（含）以上的旅游者出游报名，敬请 谅解。',
              details: ['']
            }
          ]
        }
      ]
    }
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
