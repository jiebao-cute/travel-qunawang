<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions" v-if="showSwiper">
      <swiper-slide v-for="a in swiperlist" :key="a.id">
        <img class="swiper-img" :src="a.imgUrl" alt="slow"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>

export default {
  name: 'HomeSwiper',
  props: {
    swiperlist: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination', //  将点传播出去
        loop: true, //  循环轮播
        autoplay: true, //  自动轮播
        speed: 3000 //  轮播时间
      }
    }
  },
  computed: {
    showSwiper(){
      return this.swiperlist.length
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
