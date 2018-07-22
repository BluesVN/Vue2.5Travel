<template>
<div class="wrapper">
  <swiper :options="swiperOption" >
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180713_CPM_11053.jpg'
        },
        {
          id: '0002',
          imgUrl:
            'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/dujia_shuqi_banner_20180710.jpg'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
.wrapper>>>.swiper-pagination-bullet-active
  background: #fff

.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 24.533%
  background-color: #eee

  .swiper-img
    width: 100%
</style>
