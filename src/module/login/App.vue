<template>
  <div id="app">
    	<div id="backdrop">
      <div id="wrap">
        <div id="UpdatePanel1">
          <label> 用户名:
            <input v-model="userName" type="text" class="inputtext">
          </label> 
          <label> 密码:
            <input v-model="password" type="password"  class="password">
          </label>
          <div id="error" class="error"><span>您输入的用户名或密码不正确</span></div>
          <input type="submit" class="submit" value="登陆" v-on:click="login()" onmouseover="this.className='submitOver'" onmouseout="this.className='submit'" />
        </div>
        <!--<div class="copyright">
          &copy;2016<a href="http://www.digiark.com">digiark</a>, all rights
          reserved 广州数字方舟信息技术股份有限公司
        </div>-->
      </div>
    </div>
  </div>
</template>

<script>
import "common/css/reset.css";
import "./css/login.css";

export default {
  name: "app",
  data:{
    userName:"",
    password:""
  },
  methods:{
    login:function (){
      alert(this.userName+":"+this.password);
    }
  }

};
</script>


