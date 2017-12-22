<template>
  <div class="wrap">
    <el-container>
      <el-header height="100px">
        档案审核
      </el-header>
      <el-main>
        <div style="position:absolute;z-index=1;">
          <el-table :data="tableData" stripe border style="position:relative;top:100px;left:300px;" height="500" @row-click="toClass">
            <el-table-column
              prop="name"
              label="姓名"
              width="200">
            </el-table-column>
            <el-table-column
              prop="id"
              label="学号"
              width="200">
            </el-table-column>
            <el-table-column
              prop="info"
              label="个人信息">
            </el-table-column>
          </el-table>
        </div>
        <div style="position:absolute;z-index=2">
          <el-button style="position:relative;left:1500px;top:-40px;background-color:#f7cbdb;">返回首页</el-button>
        </div>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      tableData: [{
        name: '我',
        id: 1,
        info: '点此查看个人信息'
      }, {
        name: '你',
        id: 2,
        info: '点此查看个人信息'
      }, {
        name: '他',
        id: 3,
        info: '点此查看个人信息'
      }]
    }
  }
}
</script>

<style scoped>
.el-header {
  background-color: #e8488b;
  text-align: center;
  line-height: 100px;
  font-size: 30px;
  color: #ffffff;
}
.el-main {
  background-color: #ffe8f3;
  text-align: center;
  line-height: 160px;
  height: 900px;
}
.el-table {
  width: 630px;
  font-size:20px;
}
</style>
