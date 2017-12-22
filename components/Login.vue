<template>
  <div>HHHHHHH</div>
</template>

<script>
export default {
  data () {
    return {}
  },
  mounted () {
    var url = location.href.split('?')
    this.role = url[1]
    console.log(this.role)
    switch (this.role) {
      case 'student':
        this.$router.push('/student')
        break
      case 'admin':
        this.$router.push('/admin')
        break
      case 'master':
        this.$router.push('/master')
        break
      case 'teacher':
        this.$router.push('/teacher')
        break
    }
  }
}
</script>

<style scoped>

</style>


