<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of list" :key='item.id'>
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgUrl'>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Recommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    height .75rem
    line-height .75rem
    background-color #e5e5e5
    text-indent .2rem
    margin-top .1rem
  .item-img-wrapper
    width 100%
    height 0
    padding-bottom 37.57%
    .item-img
      width 100%
  .item-info
    padding .14rem .2rem .2rem .2rem
    .item-title
      font-size .30rem
      ellipsis()
    .item-desc
      color #616161
      font-size .24rem
      margin-top .15rem
      ellipsis()
</style>
