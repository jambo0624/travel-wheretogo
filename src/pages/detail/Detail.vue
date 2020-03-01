<template>
  <div class="container">
    <detail-banner
      :sightName="sightName[this.routerId]"
      :bannerImg="bannerImg[this.routerId]"
      :bannerImgs="gallaryImgs[this.routerId]"
    ></detail-banner>
    <detail-header></detail-header>
    <detail-list :list="list[this.routerId]"></detail-list>
    <detail-declare :tips="tips"></detail-declare>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import DetailDeclare from './components/Declare'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
    DetailDeclare
  },
  data() {
    return {
      routerId: 0,
      sightName: [
        '产品编号 3174821387',
        '产品编号 2498094911',
        '产品编号 546426052',
        '产品编号 3068733325',
        '产品编号 1071628307'
      ],
      bannerImg: [
        'https://img1.qunarzz.com/vs_ceph_vs_tts/fafe9394-8e5f-4ca9-b284-0cde9e516723.jpg_r_1280x840x95_cd6f7120.jpg',
        'https://img1.qunarzz.com/p/tts0/1712/ae/14c267409541002.jpg_r_640x420x95_35833c1c.jpg',
        'https://img1.qunarzz.com/vs_ceph_vs_tts/f7d3f925-7530-4c96-a248-1d1d82615fa1.jpg_r_640x420x95_19cd7600.jpg',
        'https://img1.qunarzz.com/p/tts1/1810/a5/41f2bc0d2c6a2602.jpg_r_1280x840x95_78938fea.jpg',
        'https://img1.qunarzz.com/p/tts0/1709/cf/bdb5e5035fe94402.jpg_r_1280x840x95_920034f3.jpg'
      ],
      gallaryImgs: [
        [
          'https://img1.qunarzz.com/vs_ceph_vs_tts/fafe9394-8e5f-4ca9-b284-0cde9e516723.jpg_r_1280x840x95_cd6f7120.jpg',
          'https://img1.qunarzz.com/vs_ceph_vs_tts/9ef888c0-5965-446b-9a8f-63d1e92f45b1.jpg_r_1280x840x95_cb14b111.jpg',
          'https://img1.qunarzz.com/vs_ceph_vs_tts/abfe690d-a57c-4dd3-8e77-f1b0e396775d.jpg_r_1280x840x95_dbc77d7b.jpg'
        ],
        [
          'https://img1.qunarzz.com/p/tts0/1712/ae/14c267409541002.jpg_r_640x420x95_35833c1c.jpg',
          'https://img1.qunarzz.com/p/tts1/1712/2d/624243a4dd2c6e02.jpg_r_1280x840x95_3d340cca.jpg',
          'https://img1.qunarzz.com/p/tts4/1710/3b/d78f6558c38cb602.jpg_r_1280x840x95_3022964d.jpg'
        ],
        [
          'https://img1.qunarzz.com/vs_ceph_vs_tts/f7d3f925-7530-4c96-a248-1d1d82615fa1.jpg_r_640x420x95_19cd7600.jpg',
          'https://img1.qunarzz.com/vs_ceph_vs_tts/a5e26bf9-72d7-4df4-8d1c-0b405d1b77c5.jpg_r_1280x840x95_c8863c7b.jpg',
          'https://img1.qunarzz.com/vs_ceph_vs_tts/6e11c79d-213a-4b5a-a3b9-57c13fa2a22c.jpg_r_1280x840x95_5cb8ed94.jpg',
          'https://img1.qunarzz.com/vs_ceph_vs_tts/c35e55a8-b4d5-49ad-b7ce-14a7a5a0c17e.jpg_r_1280x840x95_c9ce620d.jpg'
        ],
        [
          'https://img1.qunarzz.com/p/tts1/1810/a5/41f2bc0d2c6a2602.jpg_r_1280x840x95_78938fea.jpg',
          'https://img1.qunarzz.com/p/tts2/1810/7c/423d30ee03eaf02.jpg_r_1280x840x95_d860293c.jpg',
          'https://img1.qunarzz.com/p/tts8/1810/d9/9026687402436302.jpg_r_1280x840x95_b52e12ed.jpg'
        ],
        [
          'https://img1.qunarzz.com/p/tts0/1709/cf/bdb5e5035fe94402.jpg_r_1280x840x95_920034f3.jpg',
          'https://img1.qunarzz.com/p/tts6/1709/9f/0c31e0a7e4dc202.jpg_r_1280x840x95_d00113d3.jpg',
          'https://img1.qunarzz.com/p/tts8/1711/ea/1874485816705d02.jpg_r_1280x840x95_0e6e0b73.jpg'
        ]
      ],
      list: [
        {
          title:
            '云南丽江泸沽湖5+N天自由行丨高端客栈&湖景房+鲜花铺床丨网红桃花酿＆下午茶',
          money: 2900
        },
        {
          title:
            '三亚纯玩0购海景房丨分界洲一整天丨南山丨天涯海角丨玫瑰谷丨海南三亚5日双飞✈跟团',
          money: 2892
        },
        {
          title:
            '西安假期特惠☞华清宫💎观乾陵法门寺💎赠耳麦电瓶+华阴老腔♥西安纯玩高铁4日游',
          money: 1710
        },
        {
          title:
            '厦门精品纯玩 厦门5日！高端酒店〈下单立减〉土楼+鼓浪屿+毓园+南普陀+曾厝垵',
          money: 3080
        },
        {
          title:
            '成都臻行纯玩☂盛世彝宴♧千年冰川♥天然温泉♬原始森林☛成都海螺沟木格措双✈6日游',
          money: 2590
        }
      ],
      tips: [
        {
          id: '0001',
          title: '特殊说明',
          subtitle: '费用不含',
          items: [
            {
              id: '0001',
              item: '【不可抗力】',
              details: [
                '因交通延阻、罢工、天气、飞机、机器故障、航班取消或更改时间等不可抗力原因所导致的额外费用'
              ]
            },
            {
              id: '0002',
              item: '【个人消费】',
              details: [
                '1、酒店内洗衣、理发、电话、传真、收费电视、饮品、烟酒等个人消费',
                '2、购物等个人消费以及因个人疏忽、违章或违法引起的经济损失或赔偿费用',
                '3、当地参加的自费项目以及 “费用包含”中不包含的其它项目'
              ]
            },
            {
              id: '0003',
              item: '【单房差】',
              details: [
                '1、单房差',
                '2、升级舱位、升级酒店、升级房型等产品的差价'
              ]
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
              details: [
                '价格：￥630起/人',
                '价格说明：儿童套餐费用只含车费，不含赠送项目和住宿，如有产生则自理。因儿童机票情况有点特殊，所以此费用是不含儿童机票，机票根据游客出行时间具体核价，看按成人价出票，还是购买儿童票划算，请致电详询供应商。'
              ]
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
              item:
                '1、60周岁（含）以上老年人预订出游，须有家属或朋友陪同方可出游; 因服务能力所限，不接受70周岁（含）以上的旅游者出游报名，敬请 谅解。',
              details: ['']
            }
          ]
        }
      ]
    }
  },
  activated() {
    this.routerId = parseInt(this.$route.params.id)
  }
}
</script>

<style lang="stylus" scoped>
.container {
  height: 100%;
  background: #e0e0e0;
}
</style>
