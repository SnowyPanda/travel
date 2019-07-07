<template>
  <div>
      <div class="banner" @click="handleBannerClick">
          <img class="banner-img" :src="bannerImg" />
          <div class="banner-info">
            <div class="banner-title">{{this.sightName}}</div>
            <div class="banner-number"><span class="iconfont banner-icon">&#xe6eb;</span>{{this.gallaryImgs.length}}</div>
          </div>
      </div>
      <fade-animation>
        <common-gallary :imgs="gallaryImgs" v-show="showGallery" @close="handleGalleryClose"></common-gallary>
      </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/Fade'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallery: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
  }
}
</script>

<style lang="stylus" scoped>
.banner
  overflow: hidden
  height: 0
  padding-bottom: 55%
  position: relative
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: .6rem
    color: #fff
    background-image: liner-gradient(top,rgba(0, 0, 0, 0), grba(0, 0, 0, 0.8))
    .banner-title
      font-size: .32rem
      padding: .2rem
      flex: 1
    .banner-number
      margin-top: 14rem
      padding: 0 .4rem
      line-height: .32rem
      height: .32rem
      border-radius: .2rem
      background: rgba(0, 0, 0, .8)
      font-size: .32rem
      .banner-icon
        font-size: .24rem
</style>
