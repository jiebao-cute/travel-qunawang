<template>
  <div class="container">
    <div class="wrapper">
      <swiper :options="swiperOptions">
        <swiper-slide>
          <img class="gallery-img" src="http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_140x140_1c863e5c.jpg" alt="slow"/>
        </swiper-slide>
        <swiper-slide>
          <img class="gallery-img" src="http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_140x140_1c863e5c.jpg" alt="slow"/>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
    gallery
  </div>
</template>
<script>
export default {
  name: 'CommonGallery',
  data () {
    return {
      swiperOptions: {
        paginationType : 'fraction',
      }
    }
  },
}
</script>
<style lang="stylus" scoped>
.container{
  display: flex
  flex-direction: column
  justify-content: center
  z-index: 99
  position: fixed
  left: 0
  top: 0
  bottom: 0
  right: 0
  background: #000000
  .wrapper{
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 100%
    .gallery-img{
      width: 100%
    }
  }
}
</style>
