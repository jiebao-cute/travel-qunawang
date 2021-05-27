<template>

  <div class="icons">
    <swiper :options="swiperOptions">
      <swiper-slide>
        <div class="icon">
          <div class="icon-img">
            <img class="icon-img-center" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png" alt="">
          </div>
          <p class="icon-decs">酒店</p>
        </div>
      </swiper-slide>
        <swiper-slide>
          <div class="icon">
            <div class="icon-img">
              <img class="icon-img-center" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png" alt="">
            </div>
            <p class="icon-decs">酒店</p>
          </div>
        </swiper-slide>
      </swiper>
     </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data() {
    return {
      swiperOptions: {
        loop: true
      },
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.icons >>> .swiper-container{
  height: 0
  padding-bottom: 50%
}
  .icon {
    position: relative
    float: left
    height: 0
    width: 25%
    padding-bottom: 25%

    .icon-img {
      position: absolute
      box-sizing: border-box
      padding: .1rem
      left: 0
      right: 0
      top: 0
      bottom: .44rem

      .icon-img-center {
        height: 100%
        display: block
        margin: 0 auto
      }
    }

    .icon-decs {
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .44rem
      height: .44rem
      color: $darkTextColor
      text-align: center
    }
}
</style>
