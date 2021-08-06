<template>
  <div class="registe">
    <div>username</div>
  <el-input v-model="username" placeholder="please input your username" id="Rusername"></el-input>
  <div class="block"></div>
  <div>password</div>
  <el-input placeholder="input your password" v-model="password1" show-password id="Rpassword"></el-input>
   <div class="block"></div>
   <div>confirm your password</div>
   <el-input placeholder="input your password again" v-model="password2" show-password></el-input>
   <div class="block"></div>
   <div>name</div>
  <el-input placeholder="input your name" v-model="name" id="Rname"></el-input>
  <div class="block"></div>
  <div>email</div>
  <el-input placeholder="input your email" v-model="email" id="Remail"></el-input>
  <div class="block"></div>
<center><div class="button"><el-button type="primary" @click="open">registe</el-button></div></center>
  </div>
</template>
<style type="text/css">
.button{
      height: 650px;
      width: 300px;
}
.block{
  height: 30px;
}
.registe{
    height: 500px;
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
      password1: ref(''),
      password2: ref(''),
      name: ref(''),
      email: ref('')
    }
  }
  ,
   methods: {
      open() {
        this.$alert('Registe successful!', 'Success', {
          confirmButtonText: 'confirm',
          callback: action => {
            this.$message({
              type: 'info',
              message: `action: ${ action }`
            });
          }
        });
      }
    }
})
</script>