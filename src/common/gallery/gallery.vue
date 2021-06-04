<template>
  <div class="container" @click="closeGallery">
    <div class="wrapper">
      <swiper :options="swiperOptions">
        <swiper-slide v-for="(item,index) of imgs" :key="index" >
          <img class="gallery-img" :src="item" alt="slow"/>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CommonGallery',
  props: {
    imgs: Array,
    default () {
      return []
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observer: true, //  观察者模式  当重新渲染时会出现滚动宽度无法计算
        observeParents: true
      }
    }
  },
  methods: {
    closeGallery () {
      this.$emit('closeGallery')
    }
  }
}
</script>
<style lang="stylus" scoped>
.container >>> .swiper-container {
  overflow: inherit
}
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
    width: 100%
    height: 0
    padding-bottom: 100%
    .gallery-img{
      width: 100%
    }
    .swiper-pagination{
      color: #ffffff
      bottom: -1rem
    }
  }
}
</style>
