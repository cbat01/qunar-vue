<template>
  <div class="header">
    <router-link
      tag="div"
      class="iconfont back-icon"
      to="./"
    >
      &#xe624;
    </router-link>
    <div class="avatar-div">
      <div class="avatar">
        <img class="avatar-img" src="https://source.qunarzz.com/usercenter/touch/avatar.png" alt="">
      </div>
    </div>
    <div class="login">登录/注册</div>
  </div>
</template>

<script>
export default {
  name: 'PersonalHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
    .header
      height: 3.2rem
      background-image: url("https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwj-kb2c1bbkAhWqJzQIHeS9CWIQjRx6BAgBEAQ&url=https%3A%2F%2Fwww.yuque.com%2Fcolorui%2Fimages&psig=AOvVaw1VBMWvQxQIsaxMQHpIIl9m&ust=1567669240737307")
      background-color: #19a9ba;
      .back-icon
        height: .8rem
        line-height: .8rem
        padding-top: .1rem
        padding-left: .4rem
        color: #ffffff
      .avatar-div
        height: 1.5rem
        .avatar
          margin: 0 auto
          width: 1.4rem
          height: 1.4rem
          border-radius: 1.4rem
          border: .08rem solid rgba(135,206,250,0.1)
          background: #fff
          .avatar-img
            width: 100%
      .login
        height .7rem
        text-align: center
        padding-top: .2rem
        color: #fff
</style>
