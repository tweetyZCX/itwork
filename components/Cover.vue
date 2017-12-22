<template>
  <div class="wrap">
    <div class="title"><span class="topic">&nbsp  &nbsp学生信息管理系统&nbsp</span><span class="welcome">欢迎你！</span></div>
    <div class="content">
      <div style="position:absolute;z-index=2;">
        <img src="../assets/cover.jpeg" width="99.6%" height="100%">
      </div>
      <div class="icons" style="position:absolute;z-index=3;">
        <img class="student" :src="student_img" @click="tologin('student')" style="position:relative;top:100px;left:350px;">
        <img class="master" :src="master_img" @click="tologin('master')" style="position:relative;top:400px;left:350px;">
        <img class="teacher" :src="teacher_img" @click="tologin('teacher')" style="position:relative;top:400px;left:430px;">
        <img class="admin" :src="admin_img" @click="tologin('admin')" style="position:relative;top:100px;left:430px;">
      </div>
      <div style="position:absolute;z-index=4;">
        <div class="choose" style="position:relative;top:130px;left:750px;font-size:40px;">
          <!-- <img src="../assets/heart.jpeg" style="width:20px;height:20px;"> -->
          请选择登录角色
        </div>
        <div style="position:relative;top:330px;left:435px;font-size:30px;color:#3f51b5">学生</div>
        <div style="position:relative;top:290px;left:1280px;font-size:30px;color:#3f51b5">管理员</div>
        <div style="position:relative;top:550px;left:680px;font-size:30px;color:#3f51b5">班主任</div>
        <div style="position:relative;top:510px;left:1000px;font-size:30px;color:#3f51b5">任课教师</div>
      </div>
      <div></div>
    </div>
  </div>
</template>

<script>
import student from '../assets/student.jpeg'
import master from '../assets/master.jpeg'
import teacher from '../assets/teacher.jpeg'
import admin from '../assets/admin.jpeg'
export default {
  data () {
    return {
      role: 'student',
      student_img: student,
      master_img: master,
      teacher_img: teacher,
      admin_img: admin
    }
  },
  methods: {
    tologin (name) {
      this.role = name
      console.log(this.role)
      this.$router.push('/' + this.role + '/login')
    }
  }
}
</script>

<style scoped>
/* .content {
  background-image: url(../assets/cover.jpeg);
  background-repeat: repeat;  
  background-size: cover;
} */

.title {
  background-color: #1a2147;
  width: 100%;
  height: 50px;
  font-family: mb-icon;
  color: #aad5e3;
  text-align: center;
  text-align: left;
}

.topic {
  font-size: 26px;
  line-height: 50px;
}
.welcome {
  font-size: 20px;
  line-height: 60px;
}

.icons img {
  border-radius: 80px;
  width: 250px;
  height: 250px;
}
</style>


