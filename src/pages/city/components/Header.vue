<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
    <p>城市选择</p>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang='stylus' scoped>
  @import '~@/assets/styles/variables.styl'
  .header
    position: relative
    overflow: hidden
    height: .86rem
    line-height: .86rem
    text-align: center
    background: $bgColor
    font-size: .32rem
    color: #fff
    .header-back
      position: absolute
      top: 0
      left: 0
      width: .64rem
      font-size: .4rem
      color: #fff
</style>
