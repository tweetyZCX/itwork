<template>
   <div class="wrap4">
     <el-container>
           <el-main>
            
            <div class="say" style="position:relative;left:50px;top:200px;">您的更改已提交，请等待审核.......</div>
            <br>
            <el-button class="ok" style="position:relative;left:40px" @click="Ok()">确定</el-button>
           
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
      this.$router.push('/student/profile')
    }
  }
}
</script>

<style scoped>

.el-main {
  background-color: #fefefe;
  color: #333;
  text-align: center;
  line-height: 160px;
}

.say {
  font-size: 60px;
  font-weight:bold;
}

.ok {

  background-color: #8fcbc4;
  width: 100px;
  height: 80px;
  font-size: 30px;
  
}

</style>
