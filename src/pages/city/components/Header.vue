<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
    城市选择
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables'
  .header
    position : relative
    overflow : hidden
    height : $headerHeight
    line-height: $headerHeight
    text-align : center
    color : #fff
    background : $bgColor
    font-size : .32rem

    .header-back
      position : absolute
      width : .64rem
      text-align: center
      font-size: 0.4rem
      color :#fff
</style>
