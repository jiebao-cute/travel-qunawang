<template>
  <div>
  <div class="title">热销推荐</div>
    <ul>
      <li>
        <div class="item border-bottom">
          <img class="item-img" src="https://imgs.qunarzz.com/wugc/p224/201207/13/f40f8a9e4327658c93835fbb.jpg_200x200_484bc04f.jpg" alt=""/>
          <div class="info">
          <p class="item-title">成都大熊猫繁育研究基地</p>
          <p class="item-desc">看！熊猫宝宝在向你招手呢</p>
            <button class="item-button">查看详情</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend'
}
</script>

<style lang="stylus" scoped>
 .title{
   background :#cacaca
   line-height: .8rem
   margin-top: .2rem
   text-indent: .2rem
 }
   .item{
     display:flex
     height: 1.9rem
     overflow: hidden
     .item-img{
       width: 1.7rem
       height: 1.7rem
       padding .1rem
     }
       .info{
         flex: 1
         padding: .1rem
         .item-title{
           line-height: .54rem
            font-size: .32rem
         }
         .item-desc{
          line-height: .44rem
           color: #cccccc
         }
         .item-button{
          line-height:  .48rem
          background :#ff9300
          padding: 0  .2rem
          margin-top: .14rem
          border-radius : .08rem
          color: #ffffff

         }
       }
   }
</style>
