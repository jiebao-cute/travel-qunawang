<template>
  <div class="header">
  <div class="header-left">
    <div class="iconfont back-icon">&#xe60e;</div>
  </div>
  <div class="header-input">
    <span class="iconfont ">&#xe614;</span>
    输入城市/景点/游玩主题</div>
    <router-link to="/city">
  <div class="header-right">{{this.city}}
  <span class="iconfont arrow-icon">&#xe615;</span>
  </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style  lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.header {
  background: $bgColor
  display: flex
  line-height: $headerHeight
  color white
  .header-left {
    width: .64rem
    float: left
    .back-icon{
      text-align: center
      font-size: .4rem
    }
  }
  .header-input {
    flex: 1
    background #ffffff
    height: .64rem
    line-height: .64rem
    border-radius: .1rem
    margin-top: .12rem
    margin-left: .2rem
    color: #ccc
    align-items: center
    padding-left: .2rem
  }
  .header-right {
    min-width: 1.24rem
    padding 0 .1rem
    float: right
    text-align center
    color: #fff
    .arrow-icon{
      font-size: .24rem
      margin-left: -.04rem
    }
  }
}
</style>
