<template>
   <div class="wrap">
     <el-container>
        <el-header height="50px"><b>{{ Name }}同学欢迎你</b> <el-button class="getout" @click="getOut()">注销</el-button></el-header>
           <el-main>
            <div style="position:absolute;z-index=1;">
                <img style="position:relative;left:10px;top:250px;" src='' alt="picture">
            <div class="myname" style="position:relative;left:500px;top:-150px;">姓名：{{ Name }}</div>
            <div class="sid" style="position:relative;left:500px;top:-200px;">学号：{{ Sid }}</div>
            <div class="sex" style="position:relative;left:500px;top:-250px;">性别：{{ Sex }}</div>
            <div class="class" style="position:relative;left:500px;top:-300px;">班级：{{ Class }}</div>
           <div class="birthday" style="position:relative;left:500px;top:-350px;">生日：{{ Birthday }}</div>
           <div class="phone" style="position:relative;left:500px;top:-400px;">手机：{{ Phone }}</div>
           <div class="telephone" style="position:relative;left:500px;top:-470px;">家庭电话：{{ Telephone }}</div>
           <div class="address" style="position:relative;left:500px;top:-550px;">地址：{{  Addres }}</div>
            <div class="introduce" style="position:relative;left:500px;top:-650px;">自我介绍：{{  Introduce }}</div>
            <el-button class="edit" style="position:relative;left:500px;top:-740px;" @click="toEdit()">编辑</el-button>
            </div>
           </el-main>

     </el-container>



   </div>
</template>

<script>
export default {
  data () {
    return {
      Name: '郭蕴喆',
      Sid: '201530613838',
      Sex: '男',
      Class: '15级软件3班',
      Phone: '11111111',
      Telephone: '10086',
      Birthday: '1993/5/10',
      Addres: '内蒙古大草原',
      Introduce: '美貌与实力并重，邪恶与恐惧的化身。四千年美男子'
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

.class {
  
  font-size: 40px;
  font-weight:bold;
}
.phone {
  
  font-size: 40px;
  font-weight:bold;
}
.telephone {
  
  font-size: 40px;
  font-weight:bold;
}
.birthday{
  
  font-size: 40px;
  font-weight:bold;
}
.address {
  
  font-size: 40px;
  font-weight:bold;
}
.introduce {
  
  font-size: 40px;
  font-weight:bold;
}
.edit {
  font-size: 40px;
  font-weight:bold;
}
</style>
