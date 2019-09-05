<template>
  <div class="list-div">
    <div class="list"
      v-for="(item, key) of spots"
      :key="key"
    >
      <div class="icon">
        <img class="icon-img" src="http://s.qunarzz.com/homenode/images/bigsearch/ticket.png" alt="">
      </div>
      <router-link
        tag="div"
        class="list-content"
        to="./"
      >
        <div class="name">
          <span class="name-main">{{item.name}}</span>
          <span class="name-detail">{{item.more}}</span>
        </div>
        <div class="price">
          <span class="price-color">￥{{item.price}}</span>
          <span class="price-gray">起</span>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchList',
  props: {
    spots: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .list-div
    padding-top: .2rem
    .list
      width: calc(100% - .3rem)
      padding-left: .3rem
      height: .84rem
      line-height: .84rem
      .icon
        width: .44rem
        height: .44rem
        float: left
        .icon-img
          width: 100%
      .list-content
        width: calc(100% - .74rem)
        height .84rem
        float: right
        .name
          width: 80%
          float: left
          font-size: .3rem
          .name-main
            font-weight: bold
          .name-detail
            font-size: .25rem
            color: #9fa2a3
            padding: .08rem
        .price
          width: 20%
          float: right
          .price-color
            color: #ff8300
          .price-gray
            color: #9fa2a3
</style>
