<template>
  <div class="box">
    <div class="title">
      <div class="iconfont iconf">
        <svg class="icon wallet-icon" aria-hidden="true">
          <use xlink:href="#iconqianbao"></use>
        </svg>
      </div>
      <div class="icon-text">我的钱包</div>
    </div>
    <div class="content">
      <div class="item">
        <div class="item-num" for="">0.00</div>
        <div class="item-text" for="">账户余额</div>
      </div>
      <div class="item">
        <div class="item-num" for="">0</div>
        <div class="item-text" for="">优惠券</div>
      </div>
      <div class="item">
        <div class="item-num" for="">0</div>
        <div class="item-text" for="">银行卡</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PersonalWallet'
}
</script>

<style lang="stylus" scoped>
  .box
    height: 2.5rem
    background: #ffffff
    margin-top: .2rem
    .title
      height: .9rem
      border-bottom: thin solid #eee
      .iconf
        width: .55rem
        height: .55rem
        margin: .18rem .2rem
        text-align: center
        float: left
        border-radius: .2rem
        background: #ff7043
        vertical-align: middle
      .wallet-icon
        display: block
        width: .4rem
        height: .4rem
        color: #ffffff
        margin-left: .09rem
        margin-top: .09rem
      .icon-text
        line-height: .9rem
        font-size: .3rem
    .content
      height: 1.6rem
      line-height 1.6rem
      padding: 0 .3rem
      .item
        display: inline-block
        height: 1.6rem
        width: 33.33%
        float: left
        .item-num
          width: 100%
          height: .8rem
          line-height: 1rem
          text-align: center
          font-size: .32rem
        .item-text
          width: 100%
          height: .8rem
          line-height: .6rem
          text-align: center
          font-size: .24rem
          color: #888
</style>
