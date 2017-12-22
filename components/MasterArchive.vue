<template>
  <div class="wrap">
    <div class="title" style="width:100%;height:100px;">修改学生档案</div>
    <div class="content" style="position:absolute;width:99.2%;height:100%;">
      <el-table :data="tableData" stripe border style="width: 360px;position:relative;top:100px;left:300px;" height="700">
        <el-table-column
          prop="date"
          label="日期"
          width="180">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          width="180">
        </el-table-column>
      </el-table>
      <el-button  style="position:relative;top:-680px;left:85%;background-color:#6895a3;color:black;" @click="toProfile()">返回首页</el-button>
      <div class="address" style="position:relative;top:-450px;left:65%;" @click="toPush()">提交申请</div>
     
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      tableData: [{
        date: '2016-05-02',
        name: '王小虎'
      }, {
        date: '2016-05-04',
        name: '王小虎'
      }, {
        date: '2016-05-01',
        name: '王小虎'
      }, {
        date: '2016-05-03',
        name: '王小虎'
      }]
    }
  },
  methods: {
    toProfile () {
      this.$router.push('/master/profile')
    },
    toPush () {
      this.$router.push('/master/push')
    }
  }
}
</script>

<style scoped>
.title {
  background-color: #6895a3;
  text-align: center;
  line-height: 100px;
  font-size: 45px;
}
.content {
  background-color: #bac6c9;
}

.address {
  width: 160px;      
  height: 140px;      
  background-color:#eef2f4;      
  border-radius: 60px;      
  font-size: 30px;
  line-height: 140px;
  color: rgb(0, 0, 0);
  text-align: center;
}
</style>
