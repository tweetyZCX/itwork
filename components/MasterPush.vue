<template>
   <div class="wrap4">
     <el-container>
           <el-main>
            
            <div class="say" style="position:relative;left:50px;top:200px;">已经帮你提交！！！</div>
            <el-button class="ok" style="position:relative;left:40px top:200px;" @click="Ok()">返回首页</el-button>
           
           </el-main>

     </el-container>



   </div>
</template>

<script>
export default {
  data () {
    return {}
  },
  methods: {
    Ok () {
      this.$router.push('/master/profile')
    }
  }
}
</script>

<style scoped>

.el-main {
  background-color: #c9effa;
  color: #333;
  text-align: center;
  line-height: 600px;
}

.say {
  font-size: 60px;
  font-weight:bold;
  font-size: 100px;
}

.ok {

  background-color: #69bbfa;
  width: 200px;
  height: 80px;
  font-size: 30px;
  
}

</style>
