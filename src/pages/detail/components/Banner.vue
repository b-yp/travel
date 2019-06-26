<template>
  <div>
    <div class="banner">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1511/51/51ad75c2b291aef490.img.jpg_600x330_d5c0f9d2.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">鸣翠湖国家湿地公园(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe62f;</span>66</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBanner'
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      color: #fff
      line-height: .6rem
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        padding: 0 .4rem
        margin-top: .14rem
        border-radius: .2rem
        background: raba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
          margin-right: .1rem
</style>
