<template>
  <div>
    <div class="list">
      <div class="list-title border-bottom" v-for="(item,index) in list" :key="index" >
       <span class="item-title-icon"></span>
        {{item.title}}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}

</script>
<style lang="stylus" scoped>
.list-title {
  line-height: .8rem
  padding: 0  .2rem
  font-size: .32rem
  .item-title-icon {
    position: relative
    left: .01rem
    top: .06rem
    display: inline-block
    width: .36rem
    height: .36rem
    background: url("http://s.qunarzz.com/piao/image/touch/sight/detail.png") 0 -.45rem no-repeat
    margin-right: .1rem
    background-size: .4rem 3rem
  }
}
</style>
