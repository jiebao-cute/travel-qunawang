<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li>
        <div class="item border-bottom" v-for="item in recommendedList" :key="item.id">
          <img class="item-img"
               :src="item.itemUrl"
               alt=""/>
          <div class="info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data (){
    return {
      recommendedList: [{
        id:'0001',
        itemUrl:'https://imgs.qunarzz.com/wugc/p224/201207/13/f40f8a9e4327658c93835fbb.jpg_200x200_484bc04f.jpg',
        title:'成都大熊猫繁育研究基地',
        desc:'看！熊猫宝宝在向你招手呢'
      },{
        id:'0002',
        itemUrl:'https://imgs.qunarzz.com/sight/p0/1811/2f/2f9b29981c3c9f85a3.img.jpg_200x200_9d91fda5.jpg',
        title:'蜈支洲岛',
        desc:'带上心爱的人来浪漫情人岛吧~'
      },{
        id:'0003',
        itemUrl:'https://imgs.qunarzz.com/sight/p0/1704/3b/3b3e66b941c284c4a3.water.jpg_200x200_28259cee.jpg',
        title:'后海村',
        desc:'品尝生猛海鲜，享受纯朴而宁静的渔村生活'
      }]
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
