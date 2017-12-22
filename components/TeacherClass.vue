<template>
  <div class="wrap">
    <el-container>
      <el-header height="100px">
        班级信息
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
          <div class="title" style="position:relative;left:1200px;top:-100px;">班级：{{className}}</div>
          <div class="count" style="position:relative;left:1200px;top:-200px;">人数：{{amount}}</div>
          <div class="address" style="position:relative;left:1100px;top:-200px;">通讯录</div>
          <div class="organization" style="position:relative;left:1350px;top:-310px;">班级职务列表</div>
          <div class="score" style="position:relative;left:1100px;top:-200px;">成绩记录</div>
          <div class="statistics" style="position:relative;left:1350px;top:-310px;">查看统计报表</div>
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
      }],
      className: '一班',
      amount: 43
    }
  },
  methods: {
    getClassInfo (id) {

    }
  },
  mounted () {
    var id = location.href.split('?')[1]
    this.getClassInfo(id)
  }
}
</script>

<style scoped>
.title {
  font-size: 30px;
  font-weight:bold;
}
.count {
  font-size: 25px;
}
.address {
  width: 100px;      
  height: 100px;      
  background-color:#e8488b;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 100px;
  color: white;
  text-align: center;
}
.organization {
  width: 130px;      
  height: 130px;      
  background-color:#eda6c0;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 130px;
  color: white;
  text-align: center;
}
.score {
  width: 100px;      
  height: 100px;      
  background-color:#de7c9f;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 100px;
  color: white;
  text-align: center;
}
.statistics {
  width: 130px;      
  height: 130px;      
  background-color:#db6597;      
  border-radius: 50%;      
  -moz-border-radius: 50%;      
  -webkit-border-radius: 50%;
  font-size: 20px;
  line-height: 130px;
  color: white;
  text-align: center;
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
  width: 630px;
  font-size:20px;
}
</style>
