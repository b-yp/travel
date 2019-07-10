<template>
  <div class="container" @click="handleGalleryClick">
    <div class="wrapper">
      <swiper :options="swiperOptions">
        <swiper-slide v-for="(item, index) in galleryImgs" :key="index">
          <img class="gallery-img" :src="item" alt="">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Gallery',
  props: {
    galleryImgs: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'frection',
        observerParents: true,
        observer: true
      }
    }
  },
  methods: {
    handleGalleryClick () {
      this.$emit('close')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container
    display: flex
    flex-direction: column
    justify-content: center
    position: fixed
    top: 0
    right: 0
    bottom: 0
    left: 0
    z-index: 99
    color: #fff
    background: #000
    .wrapper
      height: 0
      width: 100%
      padding-bottom: 100%
      background: #fff
      .gallery-img
        height: 375px
</style>
