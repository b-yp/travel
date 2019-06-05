<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1811/73/a71cd6f8ea9dcb.jpg_r_640x214_1065f1e3.jpg',
          title: '西北皇家理工',
          desc: '这个垃圾的一批'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1606/9c/d601bd634c8d50.jpg_r_640x214_909d1d4a.jpg',
          title: '西北皇家理工',
          desc: '这个垃圾的一批'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1511/14/1cf5dc2ecbfc16.jpg_r_640x214_b4b3a58a.jpg',
          title: '西北皇家理工',
          desc: '这个垃圾的一批'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    text-indent: .2rem
    background: #eee
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
