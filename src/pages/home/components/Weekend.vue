<template>
  <div>
    <div class='recommend-title'>热销推荐</div>
    <ul>
      <li class='item border-bottom' v-for='item of recommendList' :key='item.id'>
        <div class='item-img-wrapper'>
          <img :src='item.imgUrl' class='item-img' />
        </div>
        <div class='item-info'>
          <p class='item-title'>{{item.title}}</p>
          <p class='item-desc'>{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '北京温泉排行榜',
          desc: '细数北京温泉，温暖你的冬天'
        },
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '北京温泉排行榜',
          desc: '细数北京温泉，温暖你的冬天'
        },
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '北京温泉排行榜',
          desc: '细数北京温泉，温暖你的冬天'
        },
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
          title: '北京温泉排行榜',
          desc: '细数北京温泉，温暖你的冬天'
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/mixins.styl'

.recommend-title {
  margin-top: 0.2rem
  line-height: 0.8rem
  background: #ccc
  text-indent: 0.2rem
}

.item-img-wrapper {
  height: 0
  overflow: hidden
  padding-bottom: 33.9%

  .item-img {
    width: 100%
  }
}

.item-info {
  padding: 0.1rem
  min-width: 0

  .item-title {
    line-height: 0.54rem
    font-size: 0.32rem
    ellipsis()
  }

  .item-desc {
    line-height: 0.4rem
    color: #ccc
    ellipsis()
  }
}
</style>
