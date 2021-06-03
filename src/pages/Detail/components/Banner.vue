<template>
  <div class="banner">
    <img class="banner-img" src="https://img1.qunarzz.com/travel/d9/1805/4d/c5c2dd88b67b4cb5.jpg_r_480x360x95_740b9c1e.jpg" alt="">
    <div class="banner-info">
      <div class="banner-title">北京故宫（AAAAA景区）</div>
      <div class="banner-number">
        <span class="iconfont  banner-icon" >&#xe70a;</span>
        39
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
