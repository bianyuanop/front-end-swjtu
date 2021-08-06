<template>
  <div class="top">
    <el-row>
      <el-col :span="1"></el-col>

    <el-col :span="2">
      <el-button type="success" @click="directTo('/test')" icon="el-icon-edit">test</el-button>
    </el-col>
        <el-col :span="19">
      <el-button  @click="directTo('/home')" icon="el-icon-house" >home</el-button>
    </el-col>
    <el-col :span="1">
        <el-button type="text" @click="directTo('/login')" >Sign in</el-button>
    </el-col>
        <el-col :span="1">
        <el-button type="text" @click="directTo('/registe')">registe</el-button>
    </el-col>
    </el-row>
       <el-divider></el-divider>
  </div>
  <router-view/>
</template>
