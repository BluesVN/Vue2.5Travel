<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1507/fa/fa750b3a735af5d6.img.jpg_600x330_20c4a2d1.jpg">
      <div class="banner-info">
        <div class="banner-tittle">刘公岛(AAAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>12</div>
      </div>
    </div>
    <common-gallery :imgs="imgs" v-show="showGallery" @close="handleGalleryClose"></common-gallery>
  </div>
</template>
<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1507/f8/f8a8aee26515ad80.img.jpg_r_800x800_75fa0501.jpg', 'http://img1.qunarzz.com/sight/p0/1507/a0/a0c908a630941f33.img.jpg_r_800x800_ba34dece.jpg']
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
    CommonGallery
  }
}
</script>
<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
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
      background-image: linear-gradient(top, rgba(42, 206, 168, 0.8), rgba(208, 0, 112, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
