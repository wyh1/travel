<template>
  <div>
    <div class="recommend-title">热销推荐!</div>
    <ul>
      <li class="border-bottom" v-for="item of recommendList" :key='item.id'>
        <div class="item">
          <div class="item-img-wrapper">
            <img class="item-img" :src='item.imgUrl'>
          </div>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Recommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/13/448509f1ff8d30796f6c8fc574dcc0e5.jpg_200x200_cd0c23e3.jpg',
        title: '中原福塔',
        desc: '郑州管城区，五星'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/13/448509f1ff8d30796f6c8fc574dcc0e5.jpg_200x200_cd0c23e3.jpg',
        title: '中原福塔',
        desc: '郑州管城区，五星'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/13/448509f1ff8d30796f6c8fc574dcc0e5.jpg_200x200_cd0c23e3.jpg',
        title: '中原福塔',
        desc: '郑州管城区，五星'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    height .5rem
    line-height .5rem
    background-color #ccc
    text-indent .2rem
    margin-top .1rem
  .item
    display flex
    overflow hidden
    height 2.2rem
    .item-img
      width 2.0rem
      height 2.0rem
      padding .1rem
    .item-info
      margin-left .1rem
      flex 1
      min-width 0
      .item-title
        font-size .32rem
        margin-top .26rem
        height .44rem
        line-height .44rem
        ellipsis()
      .item-desc
        height .34rem
        margin-top .25rem
        ellipsis()
      .item-button
        background #ff9300
        padding 0 .1rem
        border-radius .06rem
        margin-top .25rem
</style>
