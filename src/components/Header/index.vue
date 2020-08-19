<template>
  <div class="header">
    <div class="top">
      <div class="td">
        <img class="LogOut" :src="LogOut" alt="退出登录">
      </div>

    </div>
    <div class="bottom">
      <span class="helloMessage">欢迎您，管理员：{{username}}</span>
    </div>
  </div>
</template>

<script>
  import '@/assets/css/head.css';
  import LogOut from '@/assets/images/systerm1.gif';
  export default{
    data (){
      return {
        LogOut:LogOut,
        username:'张三'
      }
    }
  }
</script>

<style lang="scss">

</style>
