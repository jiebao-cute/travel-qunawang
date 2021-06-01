<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li>
        <div class="item border-bottom" v-for="item in weekendList" :key="item.id">
          <div class="img-wrapper">
          <img class="item-img"
               :src="item.imgUrl"
               alt=""/>
          </div>
          <div class="info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  },
  data () {
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~@/assets/styles/mixins.styl"
.title {
  background: #eee
  line-height: .8rem
  text-indent: .2rem
}
.item {
  .img-wrapper{
    overflow: hidden
    height: 0
    padding-bottom: 40%
  }
  .item-img {
    width: 100%
  }
  .info {
    flex: 1
    padding: .1rem
    min-width: 0
    .item-title {
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    }
    .item-desc {
      line-height: .44rem
      color: #cccccc
      ellipsis()
    }
  }
}
</style>
