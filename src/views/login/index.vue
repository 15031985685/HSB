<template>
  <div>
    <div class="cm-header" style="background:#fff;">
      <div class="cm-center" style="padding-top:10px;">
        <div class="fl logos">
          <div class="logo"></div>
        </div>
        <div class="clear"></div>
      </div>
    </div>
    <!--/.cm-header-->
    <div class="userlogin">
      <div class="banner">
        <div class="fl banner-img">
          <div class="logo-img"></div>
        </div>
        <div class="form-box">
          <div class="login-tab-top">
            <a href="javascript:void(0);" @click="loginTaggle('userLogin')" :class="isLogin =='userLogin' ? 'hover' : ''">用户登录</a>
            <a href="javascript:void(0);" @click="loginTaggle('platformLogin')" :class="isLogin =='platformLogin' ? 'hover' : ''">平台登录</a>
          </div>
          <div class="login-tab-content">
            <keep-alive>
              <component :is="isLogin"></component>
            </keep-alive>

          </div>
        </div>
      </div>
      <!--/.banner-->
    </div>
    <!--/.userlogin-->
  </div>

</template>

<script>
  
  import '@/assets/css/adminpage.css'
  import '@/assets/css/form.css'
  import userLogin from '@/views/login/components/userLogin'
  import platformLogin from '@/views/login/components/platformLogin'
  export default {
    data() {
      return {
        isLogin:'userLogin'
      }
    },
    watch: {
      $route: {

      }
    },
    created() {
      // window.addEventListener('storage', this.afterQRScan)
    },
    mounted() {

    },
    destroyed() {
      // window.removeEventListener('storage', this.afterQRScan)
    },
    components: {
        userLogin,
        platformLogin
      },
    methods: {
      loginTaggle: function(name){
        this.isLogin = name
      }
    }
  }

</script>

<style lang="scss">
  .login-tab-top{
    text-align: center;
  }
</style>
