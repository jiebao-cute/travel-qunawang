<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe60e;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>
<style  lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.header {
  position: relative
  overflow: hidden
  background: $bgColor
  height: $headerHeight
  line-height: $headerHeight
  color: white
  text-align: center
  font-size: .34rem
  .header-back{
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
