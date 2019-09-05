<template>
  <div>
    <search-header :spots="spots"></search-header>
    <!-- <search-list :spots="spots"></search-list> -->
  </div>
</template>

<script>
import axios from 'axios'
import SearchHeader from './components/Header'
import SearchList from './components/List'
export default {
  name: 'Search',
  components: {
    SearchHeader,
    SearchList
  },
  data () {
    return {
      spots: []
    }
  },
  methods: {
    getSearchInfo () {
      axios.get('/api/spot.json')
        .then(this.handleGetSearchInfoSucc)
    },
    handleGetSearchInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.spots = data.spots
      }
    }
  },
  mounted () {
    this.getSearchInfo()
  }
}
</script>

<style lang="stylus" scoped>

</style>
