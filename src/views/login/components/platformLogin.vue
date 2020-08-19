<template>
  <div>
    <ul>
      <li><span>平台编号</span><input type="text" class="login-text" /></li>
      <li><span>操作员</span><input type="text" class="login-text" /></li>
      <li><span>密码</span><input type="password" class="login-pw" /></li>
      <li><span>验证码</span><input type="text" class="login-yzm" />
        <div class="yzm-img"><a href="javascript:myReload();"><img id="creatCheckCode" src="img/code.jpg"></a></div>
      </li>
    </ul>
    <div class="remember-box">
      <label><input name="" type="checkbox"> 记住密码</label>
      <a href="forget2.html">忘记密码？</a>
    </div>
    <div class="btn-box"><input class="login-btn" type="button" value="登录" onclick="location.href='index.html'"></div>
    <div class="login-error">密码错误</div>
  </div>

</template>

<script>
</script>

<style>
</style>
