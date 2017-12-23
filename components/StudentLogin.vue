<template>
  <div class="wrap">
    <el-container>
      <el-header height="50px"><b>学生登录</b> <el-button class="getout" @click="getOut()">注销</el-button></el-header>
      <el-main>
        <div class="login">
         <el-form :label-position="labelPosition" label-width="80px" v-model="form">

            <el-form-item class="username" label="用户名">
              <el-input v-model="form.username" style="margin-left:5px;width:400px;height:51px;"></el-input>
            </el-form-item>

            <el-form-item class="pwd" label="密码">
              <el-input type="password" v-model="form.pwd" style="margin-left:-72px;width:200px;"></el-input>
              <el-button class="pwdbtn" @click="pwdForget()">忘记密码？</el-button>
            </el-form-item>

           

            <el-form-item class="vali-code" >
              <el-input class="validateCode" v-model="form.validatecode" placeholder="请输入验证码" size="medium"></el-input>
              <img src='' alt="logo" title="点击换一张" @click="changeCode()">
            </el-form-item>

          </el-form>
          <el-button class="loginbtn" @click="login()">登录</el-button>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      labelPosition: 'right',
      form: {
        username: '',
        pwd: '',
        validatecode: ''
      }
    }
  },
  methods: {
    login () {
      this.$router.push('/student/profile')
    },
    pwdForget () {
      console.log('yes')
    },
    changeCode () {
      console.log('no')
    },
    getOut () {
      this.$router.push('/')
    }
  }
}
</script>

<style scoped>
.el-header {
  background-color: #65a8a0;
  color: #333;
  text-align:center;
  line-height: 50px;
}
.el-main {
  background-color: #dbecea;
  color: #333;
  text-align: center;
  line-height: 160px;
}
.username {
  margin-bottom: 30px;
}
.pwd {
  margin-bottom: 0px;
}
.login {
  padding: 30px 20px;
  width: 500px;
  height: 400px;
  background-color: #b7e2dd;
  margin-left: 1000px;
  margin-top: 200px;
  margin-bottom: 170px;
}
.loginbtn {
  background-color: #65a8a0;
  width: 200px;
  height: 40px;
  font-size: 18px;
}
.pwdbtn {
  background-color: #65a8a0;
  margin-top: 2px;
  height: 40px;
  
}
.pwdForget {
  text-align: right;
  text-align: top;
  height: 50px;
  margin-bottom: 0px;
}
.validateCode {
  width: 200px;
  margin-right: 154px;
}
.vali-code {
  margin-top: 20px;
  padding-left: 0px;
  margin-left: 0px;
  
}
.getout {
  background-color: #65a8a0;
  margin-left:1655px;
  height: 40px;
}
</style>
