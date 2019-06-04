<template>
  <div>
    <div class="title">热销推荐</div>
    <ul v-for="item in recommendList" :key="item.id">
      <li class="item border-bottom">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
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
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1611/43/43226663405d1dc6a3.img.jpg_200x200_c6c9d48f.jpg',
          title: '这是一个景点',
          desc: '这里真的很好玩'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1704/a6/a641422d6086b916a3.img.jpg_200x200_ba2f26e0.jpg',
          title: '这是一个景点',
          desc: '这里真的很好玩'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/52/523298a2dabc3cc3.img.jpg_200x200_ef352cab.jpg',
          title: '这是一个景点',
          desc: '这里真的很好玩'
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
  .item
    display: flex
    height: 1.9rem
    .item-img
      height: 1.7rem
      width: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
