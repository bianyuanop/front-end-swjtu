<template>
  <div class="login">
    <div class="username">
      <el-input placeholder="ID" v-model="username"></el-input>
    </div>
    <div class="password">
      <el-input placeholder="Password" v-model="password"></el-input>
    </div>
    <el-button type="primary" @click="open">Login</el-button>
  </div>
</template>

<style type="text/css">
.login {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.login > div {
  margin: 20px;
}
</style>
<script>
import { defineComponent } from 'vue'
import 'axios'
import axios from 'axios'
export default defineComponent ({
  data() {
    return {
      username: "2019112256",
      password: "123456"
    }
  },
   methods: {
      open() {
        axios.post('http://kmfls.design:8080/login', {
            StudentId: this.username,
            Password: this.password
          }, {
            'headers': {
              "Access-Control-Allow-Origin": "*"
            }
          })
          .then(function (response) {
            console.log(response);
          })
          .catch(function (error) {
            console.log(error);
          });
      }
    }
})
</script>