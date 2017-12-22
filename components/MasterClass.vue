<template>
  <div class="wrap">
    <div class="title" style="width:100%;height:100px;">班级学生列表</div>
    <div class="content" style="position:absolute;width:99.2%;height:100%;">
      <el-table :data="tableData" stripe border style="width: 800px;position:relative;top:100px;left:150px;" height="700">
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
        <el-table-column
          prop="address"
          label="地址">
        </el-table-column>
      </el-table>
      <el-button  style="position:relative;top:-680px;left:85%;background-color:#70c9e6;color:black;" @click="toProfile()">返回首页</el-button>
      <div class="address" style="position:relative;top:-450px;left:65%;" @click="toAddress()">通讯录</div>
     
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  },
  methods: {
    toProfile () {
      this.$router.push('/master/profile')
    },
    toAddress () {
      this.$router.push('/master/address')
    }
  }
}
</script>

<style scoped>
.title {
  background-color: #70c9e6;
  text-align: center;
  line-height: 100px;
  font-size: 45px;
}
.content {
  background-color: #c3e9f5;
}

.address {
  width: 160px;      
  height: 140px;      
  background-color:#90c8eb;      
  border-radius: 60px;      
  font-size: 30px;
  line-height: 140px;
  color: white;
  text-align: center;
}
</style>
