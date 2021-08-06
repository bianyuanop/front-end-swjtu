<template>
  <div class="about">
     <div class="input">
  <el-input v-model="username" placeholder="please input your username"></el-input>
  <div class="block"></div>
  <el-input placeholder="input your password" v-model="password" show-password></el-input>
</div>
  </div>
</template>
<style type="text/css">
.block{
  height: 50px;
}
.input{
    height: 600px;
    width: 300px;
    margin: auto;
}
</style>
<script>
  import { defineComponent, ref } from 'vue'

export default defineComponent ({
  setup() {
    return {
      username: ref(''),
      password: ref('')
    }
  }
})
</script>
