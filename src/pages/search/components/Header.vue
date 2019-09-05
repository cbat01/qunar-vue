<template>
  <div>
    <div class="header">
      <router-link tag="div" class="header-left" to="./">
        <div class="iconfont back-icon">&#xe624;</div>
      </router-link>
      <div class="header-input">
        <span class="iconfont search-icon">&#xe632;</span>
        <input v-model="searchText" class="search-input" type="text" placeholder="搜索景点门票">
      </div>
      <router-link tag="div" class="header-right" to="./">
      取消
      </router-link>
    </div>

    <div
      class="list"
      v-for="item of list"
      :key="item.id"
      v-show="searchText"
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
    <div class="noData" v-show="hasNoData">
      抱歉，没有搜索到相关信息
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchHeader',
  props: {
    spots: Array
  },
  data () {
    return {
      searchText: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasNoData () {
      return !this.list.length
    }
  },
  watch: {
    searchText () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.searchText) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        this.spots.forEach((value) => {
          if (value.spell.indexOf(this.searchText) > -1 || value.name.indexOf(this.searchText) > -1) {
            result.push(value)
          }
        })
        this.list = result
      }, 100)
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: $headerHeight
    padding-top: .2rem
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
        color: #9fa2a3
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      paddin-left: .2rem
      background-color: #f4f4f4
      border-radius: .1rem
      color: #000
      .search-icon
        padding-left: .12rem
        color: #a5a5a5
      .search-input
        width: calc(100% - 0.64rem)
        line-height: .64rem
        margin-bottom: .1rem
        background-color: #f4f4f4
    .header-right
      min-width: 1.04rem
      padding: .02rem .1rem 0
      float: right
      text-align: center
      color: #3f4548
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
  .noData
    width: 100%
    height: 1.04rem
    line-height: 1.04rem
    text-align: center
</style>
