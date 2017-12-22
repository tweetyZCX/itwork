<template>
   <div class="wrap">
     <el-container>
        <el-header height="50px"><b>{{ Name }}同学欢迎你</b> <el-button class="getout" @click="getOut()">注销</el-button></el-header>
           <el-main>
            <div style="position:absolute;z-index=1;">
                <img style="position:relative;left:80px;top:250px;" src='' alt="picture">
            <div class="myname" style="position:relative;left:650px;top:50px;">姓名：{{ Name }}</div>
            <div class="sid" style="position:relative;left:650px;top:-20px;">学号：{{ Sid }}</div>
            <div class="sex" style="position:relative;left:650px;top:-80px;">性别：{{ Sex }}</div>
            <div class="email" style="position:relative;left:650px;top:-150px;">联系方式：{{ Email }}</div>
            <div class="class" style="position:relative;left:650px;top:-200px;">班级：{{ Class }}</div>
            <el-button class="edit" style="position:relative;left:650px;top:-200px;" @click="toEdit()">编辑</el-button>
            </div>
           </el-main>

     </el-container>



   </div>
</template>

<script>
export default {
  data () {
    return {
      Name: ' 郭蕴喆 ',
      Sid: ' 201530613838 ',
      Sex: '男',
      Email: '222222222@2.com',
      Class: '15级软件3班'
    }
  },
  methods: {
    getOut () {
      this.$router.push('/')
    },
    toEdit () {
      this.$router.push('/student/edit')
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
.getout {
  background-color: #65a8a0;
  margin-left:1655px;
  height: 40px;
}
.el-main {
  background-color: #dbecea;
  color: #333;
  text-align: center;
  line-height: 160px;
}
.myname {
  
  font-size: 50px;
  font-weight:bold;
}

.sid {
  
  font-size: 40px;
  font-weight:bold;
}

.sex {
  
  font-size: 40px;
  font-weight:bold;
}

.email {
  
  font-size: 40px;
  font-weight:bold;
}

.class {
  
  font-size: 40px;
  font-weight:bold;
}

.edit {
  font-size: 40px;
  font-weight:bold;
}
</style>
