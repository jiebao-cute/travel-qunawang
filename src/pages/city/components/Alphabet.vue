<template>
  <ul class="list">
    <li class="item"
        v-for="(item,key) of cities"
        :key="key"
        @click="handleLetterClick"
    >{{key}}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  methods: {
    handleLetterClick (e) {
       this.$emit('change', e.target.innerText)
    }
  }

}
</script>
<style  lang="stylus" scoped>
@import "~@/assets/styles/varibles.styl"
.list {
  position: absolute
  width: .4rem
  top: 1.58rem
  right: 0
  bottom: 0
  display: flex
  flex-direction: column
  justify-content: center
  .item{
    text-align: center
    line-height: .4rem
    color: $bgColor
  }
}
</style>
