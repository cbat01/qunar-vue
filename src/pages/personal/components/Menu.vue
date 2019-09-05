<template>
  <div class="menu">
    <div class="list">
      <div class="iconfont iconf">
        <svg class="icon menu-icon" aria-hidden="true">
          <use xlink:href="#icondingdan"></use>
        </svg>
      </div>
      <div class="list-text">我的订单</div>
      <div class="icon-right">
        <svg class="icon icon-div" aria-hidden="true">
          <use xlink:href="#iconarrow-right"></use>
        </svg>
      </div>
    </div>
    <div class="list">
      <div class="iconfont iconf">
        <svg class="icon menu-icon" aria-hidden="true">
          <use xlink:href="#iconqianbao"></use>
        </svg>
      </div>
      <div class="list-text">我的退款</div>
      <div class="icon-right">
        <svg class="icon icon-div" aria-hidden="true">
          <use xlink:href="#iconarrow-right"></use>
        </svg>
      </div>
    </div>
    <div class="list">
      <div class="iconfont iconf">
        <svg class="icon menu-icon" aria-hidden="true">
          <use xlink:href="#icontubiaozhizuomoban"></use>
        </svg>
      </div>
      <div class="list-text">我的发票</div>
      <div class="icon-right">
        <svg class="icon icon-div" aria-hidden="true">
          <use xlink:href="#iconarrow-right"></use>
        </svg>
      </div>
    </div>
    <div class="list">
      <div class="iconfont iconf">
        <svg class="icon menu-icon" aria-hidden="true">
          <use xlink:href="#icongonglve"></use>
        </svg>
      </div>
      <div class="list-text">我的攻略</div>
      <div class="icon-right">
        <svg class="icon icon-div" aria-hidden="true">
          <use xlink:href="#iconarrow-right"></use>
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PersonalMenu'
}
</script>

<style lang="stylus" scoped>
  .menu
    margin-top: .2rem
    background: #fff
    .list
      height: 1rem
      line-height: 1rem
      border-bottom: thin solid #eee
      .iconf
        width: .55rem
        height: .55rem
        margin: .21rem .2rem
        text-align: center
        float: left
        border-radius: .2rem
        background: #4fc3f7
        vertical-align: middle
        .menu-icon
          display: block
          width: .4rem
          height: .4rem
          color: #ffffff
          margin-left: .09rem
          margin-top: .09rem
      .list-text
        width: calc(100% - 2rem)
        float: left
        font-size: .3rem
      .icon-right
        width: .5rem
        height: 1rem
        line-height: 1rem
        float: right
        .icon-div
          display: block
          color: #ccc
          padding-top: .36rem
</style>
