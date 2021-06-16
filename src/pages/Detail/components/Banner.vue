<template>
  <div>
  <div @click="handleChangeSwiper" class="banner">
    <img class="banner-img" :src= this.bannerImg alt="">
    <div class="banner-info">
      <div class="banner-title">{{this.sightName}}</div>
      <div class="banner-number">
        <span class="iconfont  banner-icon" >&#xe70a;</span>
        {{this.gallaryImgs.length}}
      </div>
    </div>
   </div>
    <common-gallery v-show="showGallery"  @closeGallery="closeGallery" :imgs="this.gallaryImgs"></common-gallery>
  </div>
</template>
<script>
import CommonGallery from 'common/gallery/gallery.vue'
export default {
  name: 'DetailBanner',
  components: { CommonGallery },
  props: {
    gallaryImgs: Array,
    sightName: String,
    bannerImg: String
  },
  data () {
    return {
      showGallery: false
    }
  },
  methods: {
    handleChangeSwiper () {
      this.showGallery = true
    },
    closeGallery () {
      this.showGallery = false
    }
  }
}
</script>
<style lang="stylus" scoped>
.banner{
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 55%
  .banner-img{
    width: 100%
  }
  .banner-info{
    color: #fff
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: .6rem
    background-image: linear-gradient(top , rgba(0,0,0,0), rgba(0,0,0,0.8));
    .banner-title{
      flex: 1
      font-size: .3rem
      padding 0 .2rem
    }
    .banner-number{
      line-height: .32rem
      margin: .14rem  0 .1rem 0
      padding: 0 .4rem
      border-radius: .2rem
      font-size: .24rem
      background: rgba( 0, 0, 0, .8)
      .banner-icon{
        font-size: .24rem
      }
    }
  }
}
</style>
