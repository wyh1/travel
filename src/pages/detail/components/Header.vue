<template>
  <div>
    <router-link tag="div" class="header-abs" to="/" v-show="showAbs">
      <div class="iconfont header-back-icon">&#xe624;</div>
    </router-link>
    <div class="header-fiexd" v-show="!showAbs" :style="opacityStyle">
      <router-link to="/">
        <div class="iconfont header-fiexd-icon">&#xe624;</div>
      </router-link>
      景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header-fiexd
    z-index 2
    position fixed
    top 0
    left 0
    right 0
    height $headerHeight
    line-height $headerHeight
    background $bgColor
    color #fff
    text-align center
    font-size .32rem
    .header-fiexd-icon
      position absolute
      top 0
      left 0
      width .64rem
      font-size .4rem
      text-align center
      color #fff
  .header-abs
    position absolute
    left .2rem
    top .2rem
    width .8rem
    height .8rem
    line-height .8rem
    text-align center
    border-radius .4rem
    background rgba(0, 0, 0, .6)
    .header-back-icon
      color #ffffff
      font-size .4rem
</style>
