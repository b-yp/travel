<template>
  <div class="container" @click="handleGalleryClick">
    <div class="wrapper">
      <swiper :options="swiperOptions">
        <swiper-slide>
          <img class="gallery-img" src="http://img1.qunarzz.com/sight/p0/1507/52/523298a2dabc3cc3.img.jpg_350x240_ce1de51d.jpg" alt="">
        </swiper-slide>
        <swiper-slide>
          <img class="gallery-img" src="http://img1.qunarzz.com/sight/p0/1903/b7/b7bcf3da9866f089a3.img.jpg_350x240_4db2431b.jpg" alt="">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Gallery',
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
