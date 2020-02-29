<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-list :list="list"></detail-list>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data() {
    return {
      list: [
        {
          id: '1',
          title: '成人票',
          children: [
            {
              id: '1',
              title: '成人三馆联票',
              children: [
                {
                  id: '1',
                  title: '成人AAA联票'
                },
                {
                  id: '2',
                  title: '成人BBB联票'
                }
              ]
            },
            {
              id: '2',
              title: '成人五馆联票'
            }
          ]
        },
        {
          id: '2',
          title: '学生票'
        },
        {
          id: '3',
          title: '儿童票'
        },
        {
          id: '4',
          title: '特惠票'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.content
  height 30rem
</style>
