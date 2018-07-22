<template>
<div>
  <div class="title">周末去哪</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl">
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
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
          title: '上海迪士尼乐园',
          desc: '浪漫之都大连，海洋主题乐园'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
          title: '上海迪士尼乐园',
          desc: '浪漫之都大连，海洋主题乐园'
        },
        {
          id: '0003',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
          title: '上海迪士尼乐园',
          desc: '浪漫之都大连，海洋主题乐园'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins'

.title
  line-height: 0.8rem
  margin-top: 0.2rem
  background: #eee
  text-indent: 0.2rem
.item-img-wrapper
  overflow :hidden
  height :0
  padding-bottom :37.08%
  .item-img
    width: 100%

.item-info
  padding: 0.1rem

  .item-title
    line-height: 0.54rem
    font-size: 0.32rem
    ellipsis()

  .item-desc
    line-height: 0.4rem
    color: #ccc
    ellipsis()

</style>
