<template>
  <div class="wrap3">
    <el-container>
      <el-header height="50px"><b>修改档案</b> <el-button class="getout" @click="getOut()">返回</el-button></el-header>
      <el-main>
        <div class="editpain">
         <el-form :label-position="labelPosition" label-width="100px" v-model="form">

            <el-form-item class="name" label="姓名">
              <el-input v-model="form.Name" ></el-input>
            </el-form-item>

            <el-form-item class="sid" label="学号">
              <el-input type="password" v-model="form.Sid" ></el-input>
            </el-form-item>

            <el-form-item class="sex" label="性别">
              <el-input type="password" v-model="form.Sex" ></el-input>
            </el-form-item>

            <el-form-item class="email" label="联系方式">
              <el-input type="password" v-model="form.Email" ></el-input>
            </el-form-item>

            <el-form-item class="class" label="班级">
              <el-input type="password" v-model="form.Class" ></el-input>
            </el-form-item>

          </el-form>
          <el-button class="pushbutton" @click="push()">提交</el-button>
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
        Name: '',
        Sid: '',
        Sex: '',
        Email: '',
        Class: ''
      }
    }
  },
  methods: {
    push () {
      this.$router.push('/student/push')
    },
    getOut () {
      this.$router.push('/student/profile')
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

.editpain {
  padding: 30px 20px;
  width: 500px;
  height: 400px;
  background-color: #dbecea;
  margin-left: 550px;
  margin-top: 200px;
  margin-bottom: 170px;
}
.pushbutton {
  background-color: #eff4f3;
  width: 100px;
  height: 50px;
  font-size: 20px;
}

.getout {
  background-color: #65a8a0;
  margin-left:1655px;
  height: 40px;
}
</style>
