<template>
	<view class="register-content">
		<h2>注册用户</h2>
		<view class="register-item">
			<text>用户名：</text>
			<input type="text" placeholder="请输入用户名" v-model="username">
		</view>
		<view class="register-item">
			<text>Email:</text>
			 <input type="email" placeholder="请输入邮箱" v-model="email">
		</view>
		<view class="register-item">
			<text>密码：</text>
			<input type="password" placeholder="请输入6~16位密码" v-model="password">
		</view>
		<view class="register-item">
			<text>确认密码：</text>
			<input type="password" placeholder="请在次输入您的密码" v-model="repassword">
		</view>
		<button type="default" @click="register">确认注册</button>
		<view class="register-agreement">
			<view class="agreement-icon" v-show="flag" @click="changeflag">
				<image src="../../static/nocheck-circle.png" mode=""></image>
			</view>
			<view class="agreement-icon" v-show="!flag" @click="changeflag">
				<image src="../../static/check-circle.png" mode=""></image>
			</view>
			<text>
				用户注册即代表同意
				<text style="color: dodgerblue;">
					《服务条款》
				</text>
				和
				<text style="color: dodgerblue;">
					《隐私协议》
				</text>
			</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				flag:true,
				username:'',
				email:"",
				password:'',
				repassword:""
				
			}
		},
		methods: {
			register(){
				uni.request({
					url:"https://api.shop.eduwork.cn/api/auth/register",
					method:"POST",
					data:{
						name:this.username,
						email:this.email,
						password:this.password,
						password_confirmation:this.repassword
					},
					success(res) {
						console.log(res);
						console.log("注册成功");
						uni.navigateTo({
							url:"/pages/login/login"
						})
					}
				})
			},
			
			changeflag(){
				this.flag = !this.flag
			}
		}
	}
</script>

<style lang="scss">
	
	.register-content{
		width: 100%;
		height: 100vh;
		margin-top: 20px;
		overflow: hidden;
		box-sizing: border-box;
		padding: 10px 20px;
		text-align: center;
		
		.register-item{
			width: 100%;
			padding: 10px 30px;
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			align-items: center;
			justify-content: space-between;
			margin-top: 20px;
			border-bottom: 1px solid #e0e0e0;
			
			text:{
				width: 30%;
			}
			
			input{
				width: 65%;
				text-align: left;
			}
		}
		
		button{
			margin-top: 40px;			
			width: 100%;
			border-radius: 20px;
			background-color: $base-color;
			color: #ffffff;
			font-weight: 700;
			font-size: 20px;
		}
		
		.register-agreement{
				width: 100%;
				margin-top: 30px;
				box-sizing: border-box;
				overflow: hidden;
				display: flex;
				
				
				.agreement-icon{
					width: 20px;
					height: 20px;
					overflow: hidden;
					box-sizing: border-box;
					
					image{
						width: 100%;
						height: 100%;
					}
				}
		}
	}

</style>
