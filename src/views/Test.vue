<template>
    <div class="test">  
      <el-radio v-model="radio" label="1">A</el-radio>
      <el-radio v-model="radio" label="2">B</el-radio>
      <el-radio v-model="radio" label="3">C</el-radio>
      <el-radio v-model="radio" label="4">D</el-radio>
    </div>
</template>
<script>
  export default {
    data () {
      return {
        radio: '1'
      };
    }
  }
</script>ss