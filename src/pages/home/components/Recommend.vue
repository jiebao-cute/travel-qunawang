<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
        <router-link
          tag="li"
          :to="'/detail/' + item.id"
          class="item border-bottom"
          v-for="item in recommendList"
          :key="item.id">
          <img class="item-img"
               :src="item.imgUrl"
               alt=""/>
          <div class="info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
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
  margin-top: .2rem
  text-indent: .2rem
  font-size: .3rem
}
.item {
  display: flex
  height: 1.9rem
  overflow: hidden
  padding: .1rem 0
  .item-img {
    width: 1.8rem
    height: 1.8rem
    padding .1rem
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
    .item-button {
      line-height: .48rem
      background: #ff9300
      padding: 0 .2rem
      margin-top: .14rem
      border-radius: .08rem
      color: #ffffff
    }
  }
}
</style>
