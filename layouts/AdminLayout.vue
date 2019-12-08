<template>
  <el-container style="height: 100vh;" >
    <el-aside style="background-color: #1C1C2B;" :width="asideWidth" class="hidden-md-and-down">
      <el-menu :default-openeds="['']" background-color="#1C1C2B"
      text-color="#959CB6"
      active-text-color="#5872F2" :collapse="isCollapse" >
        <el-menu-item>
          <img src="~assets/logo.png" width="18px">
          <span slot="title">Microcept</span>
        </el-menu-item>
        <nuxt-link to="/admin/dashboard" style="text-decoration:none;">
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">Dashboard</span>
          </el-menu-item>
        </nuxt-link>
        <el-submenu index="1">
          <template slot="title">
            <i class="el-icon-lock"></i>
            <span slot="title">Authentication</span>
          </template>
          <el-menu-item-group>
            <nuxt-link to="/authentication/login" style="text-decoration:none;">
              <el-menu-item index="1-1">Login</el-menu-item>
            </nuxt-link>
            <el-menu-item index="1-2">Register</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-menu-item index="3">
          <i class="el-icon-document"></i>
          <span slot="title">Navigator Three</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-setting"></i>
          <span slot="title">Navigator Four</span>
        </el-menu-item>
      </el-menu>
    </el-aside>
    
    <el-container>
      <el-header style="font-size: 12px; padding:0px 0px;line-height:40px;">
        <el-menu mode="horizontal"  text-color="#6C7293"
      active-text-color="#8095FE">
          <el-menu-item  @click="toggleSideMenu" class="hidden-md-and-down"><i class="el-icon-s-fold"></i></el-menu-item>
          <el-menu-item class="hidden-md-and-up"><i class="el-icon-s-fold"></i></el-menu-item>
          <el-menu-item index="2" style="font-weight:520;float:right;" >HI, 
              <el-avatar size="small" style="background-color:#DDEFEE;color:#0ABB87;">P</el-avatar>
          </el-menu-item>
        </el-menu>
      </el-header>
      
      <el-main>
        <nuxt/>
      </el-main>
      <el-footer>
        <el-row>
          <el-col :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
            <span>&copy; Copyright 2020</span>
          </el-col>
          <el-col :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
            Designed with <i class="fa fa-heart" style="color:#F56C6C;"></i> by <span style="color:#F05340;">Micro</span><span style="color:#41B883;">cept</span> Technologies and Education
          </el-col>
        </el-row>
      </el-footer>
    </el-container>
  </el-container>
</template>
<script>
  export default {
   data(){
    return{
      isCollapse:false,
      asideWidth:'220px',
    }
   },
   methods:{
    toggleSideMenu(){
      if(this.isCollapse){
        this.isCollapse = !this.isCollapse;
        this.asideWidth = '220px';
      }else{
        this.isCollapse = !this.isCollapse;
        this.asideWidth = '60px';
      }
     
    }
   }
  };
</script>
<style>
  .el-header {
    background-color: #FFFFFF;  
  }
  .el-menu-item{
    color: #959CB6;
  }
  .el-menu{
    border-right: 0px;
  }
  .logo{
    padding:21px 14px;
  }
  .el-container{
    font-family:Poppins,Helvetica,sans-serif;
  }
  .el-footer {
    background-color: white;
    color: #959CB6;
    text-align: center;
    line-height: 60px;
    font-size: 14px;
  }
</style>