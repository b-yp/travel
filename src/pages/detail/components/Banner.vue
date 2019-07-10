<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" alt="">
      <div class="banner-info">
        <div class="banner-title">{{ this.sightName }}</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe62f;</span>
          {{ this.galleryImgs.length }}
        </div>
      </div>
    </div>
    <common-gallery
      :galleryImgs="galleryImgs"
      v-show="showGallery"
      @close="handleGalleryClose"
    ></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    galleryImgs: Array
  },
  data () {
    return {
      showGallery: false
    }
  },
  components: {
    CommonGallery
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  }
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
