<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="(item, index) of list" :key="index">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="" />
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
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import "../../../assets/styles/mixins.styl"
.title
  line-height .8rem
  background #eee
  padding-left .2rem
.item-img-wrapper
  height 0
  overflow hidden
  padding-bottom 37.9%
.item-img
  width 100%
.item-info
  flex 1
  padding 0.2rem 0.2rem
  .item-title
    line-height .48rem
    font-size .34rem
    ellipsis()
  .item-desc
    line-height .4rem
    font-size .24rem
    ellipsis()
</style>
