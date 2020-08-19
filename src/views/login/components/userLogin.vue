<template>
  <div>
    <ul>
      <li><span>平台编号</span><input type="text" class="login-text" /></li>
      <li><span>手机号</span><input type="text" class="login-text" /></li>
      <li><span>用户编号</span><input type="text" class="login-text" /></li>
      <li><span>密码</span><input type="password" class="login-pw" /></li>
      <li><span>验证码</span><input type="text" class="login-yzm" />
        <div class="yzm-img"><a href="javascript:myReload();"><img id="creatCheckCode" src="img/code.jpg"></a></div>
      </li>
    </ul>
    <div class="remember-box">
      <label><input name="" type="checkbox"> 记住密码</label>
      <a @click="goPassword('userLogin')">忘记密码？</a>
    </div>
    <div class="btn-box"><input class="login-btn" type="button" value="登录"></div>
    <div class="login-error">{{loginError}}</div>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        loginError:''
      }
    },
    mounted() {
    },
    methods: {
      goPassword(id){
        this.$router.push(`/forgotPassword/${id}`)
      }
    }
  }

</script>

<style>
</style>
