<template>

  <div class="icons">
    <swiper :options="swiperOptions">
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-center" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-decs">{{ item.decs }}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOptions: {
        loop: true
      },
      iconList: [
        {id: '001',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/hotel.png',
          decs: '酒店'
        },
        {id: '002',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/flight.png',
          decs: '机票'
        },
        {id: '003',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/train.png',
          decs: '火车票'
        },
        {id: '004',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          decs: '度假'
        },
        {id: '005',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/piao.png',
          decs: '景点门票'
        },
        {id: '006',
          imgUrl: 'https://picbed.qunarzz.com/f5e5770393d759578962e53ee67798c8.png',
          decs: '海外酒店'
        },
        {id: '007',
          imgUrl: 'https://picbed.qunarzz.com/a36d2288f19e54562338f4d8ef986288.png',
          decs: '低价机票'
        },
        {id: '008',
          imgUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png',
          decs: '汽车船票'
        },
        {id: '009',
          imgUrl: 'https://picbed.qunarzz.com/ae617a31e0bd5803d76918b817f6d942.png',
          decs: '自由行'
        }
      ]
    }
  },
  computed: {
    pages () { // 将每八个item分为一个page
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
@import "~@/assets/styles/mixins.styl"
.icons >>> .swiper-container {
  height: 0
  padding-bottom: 50%
}

.icon {
  position: relative
  float: left
  height: 0
  width: 25%
  padding-bottom: 25%

  .icon-img {
    position: absolute
    box-sizing: border-box
    padding: .1rem
    left: 0
    right: 0
    top: 0
    bottom: .44rem

    .icon-img-center {
      height: 100%
      display: block
      margin: 0 auto
    }
  }

  .icon-decs {
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: .44rem
    height: .44rem
    color: $darkTextColor
    text-align: center
    ellipsis()
  }
}
</style>
