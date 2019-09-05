<template>
  <div class="header">
    <router-link tag="div" class="header-left" to="./personal">
      <div class="iconfont back-icon">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icontubiaozhizuomoban"></use>
        </svg>
      </div>
    </router-link>
    <router-link tag="div" class="header-input" to="./search">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </router-link>
    <router-link to='/city'>
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
        padding-left: .2rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
</style>
