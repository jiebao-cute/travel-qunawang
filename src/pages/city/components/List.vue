<template>
  <div class="list">
    <div class="area">
      <div class="title border-topbottom" >当前城市</div>
      <div class="button-list">
        <div class="button-wrapper">
        <div class="button">成都</div>
        </div>
        <div class="button-wrapper">
          <div class="button">成都</div>
        </div>
        <div class="button-wrapper">
          <div class="button">成都</div>
        </div>
        <div class="button-wrapper">
          <div class="button">成都</div>
        </div>

      </div>
    </div>

    <div class="area">
      <div class="title border-topbottom">热门城市</div>
      <div class="button-list">
       <div class="button-wrapper">
        <div class="button">成都</div>
       </div>
      </div>
    </div>

    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
        <div class="item border-bottom"> 阿拉尔</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList',
}
</script>
<style  lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.border-topbottom{
  &:before{
    border-color: #ccc
  }
  &:after{
    border-color: #ccc
  }
}
.list {
  overflow: hidden
  position:absolute
  top: 1.58rem
  right: 0
  left: 0
  bottom: 0
  .title {
    background: #eeeeee
    line-height: .44rem
    color: #666
    font-size: .26rem
    padding-left: .2rem
  }

  .button-list {
    padding: .1rem .6rem .1rem .1rem
    overflow: hidden

    .button-wrapper {
      float: left
      width: 33.33%

      .button {
        padding: .1rem 0
        margin: .1rem
        text-align: center
        border: .02rem solid #cacaca
        border-radius: .06rem
      }
    }
  }

  .border-bottom {
    &:before {
      border-color: #ccc
    }
  }

  .item-list {
    .item {
      line-height: .76rem
      color: #666
      padding-left: .2rem
    }
  }
}
</style>
