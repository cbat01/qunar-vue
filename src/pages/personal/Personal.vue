<template>
  <div class="body">
    <personal-header></personal-header>
    <personal-wallet></personal-wallet>
    <personal-menu></personal-menu>
    <personal-footer></personal-footer>
  </div>
</template>

<script>
import PersonalHeader from './components/Header'
import PersonalWallet from './components/Wallet'
import PersonalMenu from './components/Menu'
import PersonalFooter from './components/Footer'
export default {
  name: 'personal',
  components: {
    PersonalHeader,
    PersonalWallet,
    PersonalMenu,
    PersonalFooter
  }
}
</script>

<style lang="stylus" scoped>
  .body
    position: fixed
    width: 100%
    height: 100%
    top: 0
    background: #ebeced
</style>
