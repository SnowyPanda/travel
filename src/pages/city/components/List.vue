<template>
    <div class="list" ref="wrapper">
        <div>
            <div class="area">
                <div class="title border-topbottom">当前城市</div>
                <div class="button-list">
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">热门城市</div>
                <div class="button-list">
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">A</div>
                <div class="item-list">
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">A</div>
                <div class="item-list">
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">A</div>
                <div class="item-list">
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">A</div>
                <div class="item-list">
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                    <div class="item border-bottom">
                        阿拉
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .border-bottom
    &:before
      border-color: #ccc
  .list
    position: absolute
    overflow: hidden
    top: 1.58rem
    bottom: 0
    right: 0
    left: 0
    .title
        line-height: .54rem
        background: #eee
        color: #666
        font-size: .26rem
        padding-left: .2rem
    .button-list
        padding: .1rem
        overflow: hidden
        padding: .1rem .6rem .1rem .1rem
        .button-wrapper
            float: left
            width: 33.33%
            .button
                text-align: center
                padding: .1rem 0
                border-radius: .06rem
                margin: .1rem
                border: .02rem solid #cccccc
    .item-list
        .item
            line-height: .76rem
            color: #666
            padding-left: .2rem
</style>
