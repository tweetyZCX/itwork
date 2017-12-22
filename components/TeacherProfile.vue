<template>
  <div class="wrap">
    <el-container>
      <el-header height="100px">
        班级列表
      </el-header>
      <el-main>
        <div style="position:absolute;z-index=1;">
          <el-table :data="tableData" stripe border style="position:relative;top:100px;left:300px;" height="500" @row-click="toClass">
            <el-table-column
              prop="className"
              label="班级"
              width="330">
            </el-table-column>
          </el-table>
        </div>
        <div style="position:absolute;z-index=2">
          <el-button style="position:relative;left:0px;top:-40px;background-color:#f7cbdb;">注销</el-button>
          <div class="tip" style="position:relative;left:1000px;top:50px;">点击班级名字进入班级页面哦！</div>
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
        classId: 1,
        className: '15级软件工程3班'
      }, {
        classId: 2,
        className: '15级软件工程4班'
      }, {
        classId: 3,
        className: '14级经贸6班'
      }]
    }
  },
  methods: {
    toClass (row) {
      console.log(row.className)
      this.$router.push('/teacher/class?id=' + row.classId)
    }
  }
}
</script>

<style scoped>
.tip {
  font-size: 30px;
  color: #e8488b;
}
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
  width: 330px;
  font-size:20px;
}
</style>
