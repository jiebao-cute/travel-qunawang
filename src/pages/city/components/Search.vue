<template>
  <div>
  <div class="search" >
   <input v-model="keyword" class="search-input" type="text" placeholder="输入城市名或拼音"/>
  </div>
  <div class="search-content" ref="search" v-show="keyword">
    <ul>
      <li class="search-item border-bottom"
          v-for="item in list"
          @click="handleCityClick(item.name)"
          :key="item.id"
      >{{item.name}}</li>
      <li class="search-item border-bottom" v-show="showWord">没有匹配的城市</li>
    </ul>
  </div>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  methods: {
    handleCityClick (city) {
      this.changeCity(city)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  computed: {
    showWord () {
      return !this.list.length
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  },
  updated () {
    this.scroll.refresh()
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  }
}
</script>
<style  lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.search {
  overflow: hidden
  background: $bgColor
  height: .72rem
  padding: 0 .1rem
  .search-input{
    box-sizing: border-box
    height: .62rem
    line-height: .62rem
    width: 100%
    text-align: center
    border-radius: .08rem
    color: #666
    padding: 0 .1rem
  }
}
  .search-content{
    z-index: 1
    position: absolute
    overflow: hidden
    top: 1.58rem
    right: 0
    bottom: 0
    left: 0
    background: #cccccc
    .search-item{
      line-height: .62rem
      padding-left: .2rem
      color: #666
      background: #ffffff
    }
  }
</style>
