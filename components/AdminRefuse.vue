<template>
  <div class="wrap">
    <div>
      <el-button class="return">返回上一页</el-button>
      <div class="why">为什么拒绝我？</div>
      <el-input class="input" type="textarea" :autosize="{ minRows: 20}" placeholder="请输入内容" v-model="reason"></el-input>
      <el-button class="send">发送</el-button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      reason: ''
    }
  },
  mounted () {

  }
}
</script>

<style scoped>
.return {
  margin-top: 20px;
  margin-left: 80%;
  background: #eb8610;
}
.send {
  margin-top: 20px;
  margin-left: 22%;
  background: #eb8610;
}
.input {
  margin-top: 50px;
  margin-left: 400px;
  width: 800px;
  display: block;
}
.why {
  margin-top: 50px;
  margin-left: 200px;
  height: 100px;
  line-height: 100px;
  font-size: 75px;
  font-style: oblique;
  font-weight: bold;
}
.wrap {
  background: #CA7853;
  height: 974px;
}
</style>
