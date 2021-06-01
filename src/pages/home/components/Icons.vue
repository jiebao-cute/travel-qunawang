<template>
  <div class="icons">
    <swiper :options="swiperOptions">
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-center" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-decs">{{ item.desc }}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props:{
    list: []
  },
  data () {
    return {
      swiperOptions: {
        loop: true
      }
    }
  },
  computed: {
    pages () { // 将每八个item分为一个page
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
@import "~@/assets/styles/mixins.styl"
.icons >>> .swiper-container {
  height: 0
  padding-bottom: 50%
}
.icons {
  margin-top: .1rem
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
      ellipsis()
    }
  }
}
</style>
