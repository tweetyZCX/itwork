<template>
  <div class="wrap">
    <el-container>
      <el-header height="100px">
        尊贵的王，欢迎登录
      </el-header>
      <el-main>
        <div style="position:absolute;z-index=1">
          <div class="archive" style="position:relative;left:840px;">导入学生档案</div>
          <div class="userInfo" style="position:relative;left:650px;">导入用户信息</div>
          <div class="check" style="position:relative;left:1080px;top:-130px;" @click="toArchiveRequests()">档案审核</div>
          <el-button style="position:relative;left:1500px;top:-430px;background-color:#f0a44a;" @click="exit()">注销</el-button>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      name: 'admin'
    }
  },
  methods: {
    exit () {
      this.$router.push('/')
    },
    toArchiveRequests () {
      this.$router.push('/admin/requests')
    }
  }
}
</script>

<style scoped>
.archive {
  width: 140px;      
  height: 140px;      
  background-color:#eb8610;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 140px;
  color: white;
  text-align: center;
}
.userInfo {
  width: 140px;      
  height: 140px;      
  background-color:#edc28e;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 140px;
  color: white;
  text-align: center;
}
.check {
  width: 100px;      
  height: 100px;      
  background-color:#c29663;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 100px;
  color: white;
  text-align: center;
}
.el-header {
  background-color: #f0a44a;
  text-align: center;
  line-height: 100px;
  font-size: 30px;
  color: #ffffff;
}
.el-main {
  background-color: #ffffff;
  text-align: center;
  line-height: 160px;
  height: 900px;
}
</style>
