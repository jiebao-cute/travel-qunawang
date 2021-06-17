<template>
  <div>
   <detail-banner :sightName="sightName" :bannerImg="bannerImg" :gallaryImgs="gallaryImgs"></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="categoryList"></detail-list>
    </div>
  </div>
</template>
<script>
import DetailBanner from './components/Banner.vue'
import DetailHeader from './components/Header.vue'
import DetailList from './components/List.vue'
export default {
  name: 'Detail',
  components: { DetailBanner, DetailHeader, DetailList },
  data () {
    return {
      sightName: '大连圣亚海洋世界(AAAA景区)',
      bannerImg: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg',
      gallaryImgs: ['http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_800x800_70debc93.jpg', 'http://img1.qunarzz.com/sight/p0/1709/76/7691528bc7d7ad3ca3.img.png_800x800_9ef05ee7.png'],
      categoryList: [{
        "title": "成人票",
        "children": [{
          "title": "成人三馆联票",
          "children": [{
            "title": "成人三馆联票 - 大连连锁店销售"
          }]
        },{
          "title": "成人五馆联票"
        }]
      }, {
        "title": "学生票",
        "children": [{
          "title": "学生五馆联票",
          "children": [{
            "title": "学生三馆联票 - 成都连锁店销售"
          }]
        },{
          "title": "学生全馆联票"
        }]
      }, {
        "title": "儿童票",
        "children": [{
          "title": "儿童联票",
          "children": [{
            "title": "儿童联票 - 青岛连锁店销售"
          }]
        },{
          "title": "儿童畅享免票"
        }]
      }, {
        "title": "特惠票"
      }]
    }
  },
  methods: {
  //   getListInfo () {
  //     axios.get('/api/detile.json', {
  //       params: {
  //         id: this.$route.params.id
  //       }
  //     })
  //       .then(this.getListInfoSucc)
  //   },
  //   getListInfoSucc (res) {
  //     res = res.data
  //     if (res.ret && res.data) {
  //       const data = res.data
  //       this.sightName = data.sightName
  //       this.bannerImg = data.bannerImg
  //       this.gallaryImgs = data.gallaryImgs
  //       this.categoryList = data.categoryList
  //     }
  //   }
  // },
  // mounted () {
  //   this.getListInfo()
   }
}
</script>
<style lang="stylus" scoped>
.content{
  height: 50rem
}
</style>
