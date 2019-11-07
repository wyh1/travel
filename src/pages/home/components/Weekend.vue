<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of recommendList" :key='item.id'>
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/86/57819390ea997c.jpg_r_640x214_00888590.jpg',
        title: '郑州打卡',
        desc: '日月轮回，孕育出新的美丽'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1711/28/461d4956ad23d8.jpg_r_640x214_d9aae5e7.jpg',
        title: '河南泡汤圣地',
        desc: '养生养颜美容温泉，东南亚异域风情，营造浪漫动感之旅，人与自然和谐相处，阳光与灿烂微笑，绿色心情与您同在'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/2c/e5e2b086fc0c60.jpg_r_640x214_811a2da7.jpg',
        title: '石刻艺术宝库',
        desc: '这里是中国石刻艺术宝库，石窟的规模大、艺术精湛，石刻艺术奇葩，是石刻艺术的典范之作。'
      }]
    }
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
