<template>
  <div>
    <router-link to="/" v-show="showAbc">
  <div class="header-abc">
    <div class="iconfont header-icon-abs">&#xe60e;</div>
  </div>
    </router-link>
  <div class="header-fixed" v-show="!showAbc" :style="opacityStyle">景点详情
    <router-link to="/">
      <div class="iconfont header-fixer-back">&#xe60e;</div>
    </router-link>
  </div>
  </div>
</template>
<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbc: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbc = false
      } else { this.showAbc = true }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>
<style lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.header-abc {
  position: absolute
  left: .2rem
  top: .2rem
  width .8rem
  height: .8rem
  border-radius: .4rem
  line-height: .8rem
  text-align: center
  background: rgb(0,0,0,.8)
  .header-icon-abs{
    color: #ffffff
    font-size: .4rem
  }
}
.header-fixed {
  z-index: 2
  position: fixed
  top: 0
  left: 0
  right: 0
  overflow: hidden
  background: $bgColor
  height: $headerHeight
  line-height: $headerHeight
  color: white
  text-align: center
  font-size: .34rem
  .header-fixer-back {
    box-sizing: border-box
    position: absolute
    top: 0
    left: 0
    width: .64rem
    text-align: center
    font-size: .4rem
    color: #ffffff
  }
}
</style>
