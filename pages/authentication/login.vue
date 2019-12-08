<template>
	<el-container>
		<el-row>
			<el-col :xs="24" :sm="24" :md="24" :lg="8" :xl="8"> 
				<div class="form-div">
					<el-card>
						<div class="logo">
							<img src="~assets/logo.png" width="50px">
						</div>
						<div class="form-content">
							<div class="title-head">
								<h4>Welcome To Microcpet Dashboard</h4>
							</div>
							<div class="title-login">
							    <p>Please enter your login details</p>
							</div>
							<div class="form">
								<el-form ref="form" >
								  <el-form-item>
								    <el-input v-model="email" placeholder="Email" type="email" prefix-icon="el-icon-s-promotion"></el-input>
								  </el-form-item>
								  <el-form-item>
								    <el-input v-model="password" placeholder="Password" type="password" prefix-icon="el-icon-unlock"></el-input>
								  </el-form-item>
								  <el-form-item>
								    <el-checkbox v-model="checked" style="float:left;">Remember Me</el-checkbox>
								    <span style="float:right;"><a href="" style="text-decoration:none;color:#B4B4B4;">Forgot your password ?</a></span>
								  </el-form-item>
								  <el-form-item>
								  	<div class="submit-btn">
								  		<el-button type="success" round>Log In</el-button>
								  	</div>
								  </el-form-item>
								</el-form>
							</div>
						</div>
					</el-card>
					<p class="footer">&copy; Copyright 2020</p>
					<p class="footer">Designed with <i class="fa fa-heart" style="color:#F56C6C;"></i> by <span style="color:#F05340;">Micro</span><span style="color:#41B883;">cept</span> Technologies and Education</p>
				</div>
			</el-col>
		</el-row>
	</el-container>
</template>
<script>
	export default{
		layout:'AuthLayout',
		data(){
			return{
				email:'',
				password:'',
			}
		}
	}
</script>
<style scoped>
    .form-content{
       
    }
	.el-container{
		height: 100vh;
		justify-content: center;
		font-family:Poppins,Helvetica,sans-serif;
		width:100%;
	}
	.el-row{
		height:100vh;
		width:100%;
		justify-content:center;
		display:flex;
	}
	.el-col{
		height:100vh;
	}
	.form-div{
		display:flex;
		flex-direction:column;
		justify-content:center;
		height:100vh;
	}
	.title-login{
		color:#B4B4B4;
		font-size:14px;
		text-align:center;
		margin-bottom:18px;
	}
	.title-head{
		color:#212121;
		text-align:center;
		margin-bottom:16px;
	}
	.submit-btn{
		justify-content:center;
		display:flex;
	}
	.logo{
		display:flex;
		justify-content:center;
	}
	.footer{
		background-color: white;
	    color: #959CB6;
	    text-align: center;
	    line-height: 30px;
	    font-size: 14px;
	}
</style>