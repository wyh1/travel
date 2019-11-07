<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="请输入城市">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .search
    background $bgColor
    height .72rem
    padding 0 .1rem
    .search-input
      box-sizing border-box
      padding 0 .2rem
      text-align center
      width 100%
      height .62rem
      line-height .62rem
      border-radius .06rem
      color #666
</style>
