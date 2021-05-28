<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li>
        <div class="item border-bottom" v-for="item in recommendedList" :key="item.id">
          <div class="img-wrapper">
          <img class="item-img"
               :src="item.itemUrl"
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
  data () {
    return {
      recommendedList: [{
        id: '0001',
        itemUrl: 'https://n1-q.mafengwo.net/s18/M00/56/DC/CoUBYGCs52OASazLACTVA0VC5T8493.png?imageMogr2%2Fthumbnail%2F%21750x422r%2Fgravity%2FCenter%2Fcrop%2F%21750x422%2Fquality%2F90',
        title: '尊享0自费🌻畅游昆大丽6日🔥甄选五钻+升级VIP陆地头等舱+送三大演出',
        desc: '看！熊猫宝宝在向你招手呢'
      }, {
        id: '0002',
        itemUrl: 'https://b1-q.mafengwo.net/s18/M00/51/9C/CoUBYGCvhoyAAl6qAB8jpSVFa0M233.png?imageMogr2%2Fthumbnail%2F%21750x422r%2Fgravity%2FCenter%2Fcrop%2F%21750x422%2Fquality%2F90',
        title: '全程0自费✦昆明+大理+丽江6日|省内双动+甲壳虫旅拍|丽江千古情+印象丽江',
        desc: '带上心爱的人来浪漫情人岛吧~'
      }, {
        id: '0003',
        itemUrl: 'https://n1-q.mafengwo.net/s18/M00/76/3D/CoUBYGCuWT2AA54vACXTjCQ28Bk151.png?imageMogr2%2Fthumbnail%2F%21750x422r%2Fgravity%2FCenter%2Fcrop%2F%21750x422%2Fquality%2F90',
        title: '昆大丽高品游👍清凉夏日新升级丨五星酒店+温泉丨私人游艇+雪山大索+花海旅拍',
        desc: '早订7天减50元'
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
