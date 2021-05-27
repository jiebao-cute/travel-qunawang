<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="a in swiperList" :key="a.id">
        <img class="swiper-img" :src="a.imgUrl" alt="slow"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>

export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination', //  将点传播出去
        loop: true, //  循环轮播
        autoplay: true, //  自动轮播
        speed: 3000 //  轮播时间
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/c77891ece9fb3abd9c7156f1588f5732.jpeg'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/f8bd77048382f0a8ab109f860f04a88f.jpeg'
      }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active { //穿透scoped改变点的颜色
  background: #ffffff
}

.wrapper {
  width: 100%
  height: 31.25vm

  .swiper-img {
    width: 100%
  }
}

</style>
