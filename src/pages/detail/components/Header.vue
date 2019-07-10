<template>
  <div>
    <router-link
      tag="div"
      to="/"
      class="header-abs"
    >
      <div class="iconfont">&#xe624;</div>
    </router-link>
    <div class="header-fixed" v-show="showFixed" :style="opacityStyle">
      <router-link tag="div" to="/" class="iconfont header-fixed-back">&#xe624;</router-link>
      景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showFixed: false,
      opacityStyle: 0
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity: opacity }
        this.showFixed = true
      } else {
        this.showFixed = false
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/variables.styl"
  .header-abs
    position: absolute
    left: .2rem
    top: .2rem
    width: .8rem
    height: .8rem
    background: rgba(0, 0, 0, .8)
    border-radius: .4rem
    color: #fff
    line-height: .8rem
    text-align: center
  .header-fixed
    z-index: 2
    position: fixed
    left: 0
    top: 0
    right: 0
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    font-size: .32rem
    color: #fff
    text-align: center
    .header-fixed-back
      position: absolute
      left: 0
      top: 0
      width: .64rem
      text-align: center
      font-size: .4rem
      color: #fff
</style>
