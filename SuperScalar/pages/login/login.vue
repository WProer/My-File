<template>
	<view class="register-content">
		<view class="register-logo">
			<view class="logo">
				<image src="../../static/logo.png" mode=""></image>
			</view>
			<text>
				晨旭
			</text>
		</view>

		<view class="catchphrase">
			<text>学在苦中求，艺在苦中练</text>
		</view>

		<view class="information">
			<view class="information-item">
				<input type="text" placeholder="用户名" v-model="username">
			</view>
			<view class="information-item">
				<input type="email" placeholder="邮箱" v-model="email">
			</view>
			<view class="information-item">
				<input type="password" placeholder="密码" v-model="password">
			</view>
		</view>

		<view class="register-button">
			<button type="default" @click="login">登录</button>
			<button type="default" @click="toregister">注册</button>
		</view>

		<view class="register_Other_methods">

			<text>其他登录方式</text>
			<view class="other_content">
				<view class="other-content_item">
					<image src="../../static/QQ.png" mode=""></image>
				</view>
				<view class="other-content_item">
					<image src="../../static/Weixin.png" mode=""></image>
				</view>
			</view>
		</view>


		<!-- <h2>用户登录</h2>
		<label for="">用户名：<input type="text" v-model="username"></label><br>
		<label for="">登录密码：<input type="password" v-model="password"></label>
		<button @click="login()">登录</button>
		<h4>提示信息:<span style="color:red;">{{info}}</span></h4> -->
	</view>
</template>

<script>
	export default {
			data() {
				return {
					username:"",
					email:"",
					password:""
				}
			},
			onLoad() {
				
			},
			onReady() { 
			},
			methods: {
				login() {
					uni.request({
						url:"https://api.shop.eduwork.cn/api/auth/login",
						method:"POST",
						data:{
							username:this.username,
							email:this.email,
							password:this.password
						},
						success(res) {
							console.log(res);
							console.log("请求成功");
							if(res.statusCode==200){
								uni.setStorageSync("token",res.data.access_token);
								uni.showToast({
									icon:'success',
									title:"登录成功",
									duration:2000
								}),
								uni.switchTab({
									url:"/pages/index/index"
								})
								
							}else{
								uni.showToast({
									icon:'error',
									title:"登陆失败",
									duration:2000
								})
							}
						}
					})
				},
			
			
				toregister(){
					uni.navigateTo({
						url:"/pages/register/register"
					})
				}
			}
		}
</script>

<style lang="scss">
	// $text-Color-one:#3289e7;
	$text-Color-one:#99CCFF;
	$input-bgc:#c2f1ff;
	$text-shadow:#bdd8ff;
	


	.register-content {
		width: 100%;
		height: 100vh;
		padding: 10px 30px;
		overflow: hidden;
		box-sizing: border-box;
		// background-color: $base-color;
		background-color: #fff;
		position: relative;

		.register-logo {
			width: 100%;
			display: flex;
			justify-content: center;
			align-items: center;
			overflow: hidden;
			box-sizing: border-box;
			margin-top: 200px;

			.logo {
				flex-shrink: 0;
				width: 100px;
				height: 100px;
				overflow: hidden;
				box-sizing: border-box;

				image {
					width: 100%;
					height: 100%;
					overflow: hidden;
					box-sizing: border-box;
				}

			}

			text {
				flex-shrink: 0;
				// color: #fff;
				color: $base-color;
				font-family: STXingkai;
				font-size: 50px;
				font-weight: 700;
				text-shadow: 6px -2px 3px $text-shadow;
			}
		}

		.catchphrase {
			width: 100%;
			display: flex;
			justify-content: center;
			align-items: center;
			overflow: hidden;
			box-sizing: border-box;
			margin: 30px 0px;

			text {
				// color: #fff;
				color: $base-color;
				font-weight: 700;
				font-size: 25px;
				font-style: italic;
				text-shadow: 6px -2px 3px $text-shadow;

			}

		}

		.information {
			width: 100%;
			overflow: hidden;
			box-sizing: border-box;
			padding: 10px;

			.information-item {
				width: 100%;
				padding: 10px 30px;
				display: flex;
				align-items: center;
				overflow: hidden;
				box-sizing: border-box;

				input {
					margin-left: 10px;
					width: 100%;
					padding: 0px 5px;
					box-sizing: border-box;
					overflow: hidden;
					border-radius: 5px;
					// background-color: #e6f8e6;
					background-color: $input-bgc;
				}
			}
		}

		.register-button {
			width: 100%;
			overflow: hidden;
			box-sizing: border-box;
			padding: 20px 15px;
			display: flex;
			align-items: center;

			button {
				color: #ffffff;
				// background-color: #80ff80;
				background-color: $text-Color-one;
				font-weight: 700;
			}
		}

		.register_Other_methods {
			width: 100%;
			overflow: hidden;
			box-sizing: border-box;
			padding: 10px 30px;
			text-align: center;
			position: absolute;
			bottom: 10px;
			left: 0px;
			right: 0px;

			text {
				width: 100%;
				font-size: 10px;
				font-weight: 700;
				color: #a7a7a7;
				
				&::after{
					content: "————————";
					position: absolute;
					width: 100px;
					height: 1px;
					color: #ccc;
					top: 13px;
					bottom: 10px;
					right: 55px;
				}
				
				&::before{
					content: "————————";
					position: absolute;
					width: 100px;
					height: 1px;
					color: #ccc;
					top: 13px;
					bottom: 10px;
					left: 55px;
				}
			}

			.other_content {
				width: 100%;
				overflow: hidden;
				box-sizing: border-box;
				display: flex;
				align-items: center;
				justify-content: center;
				margin-top: 8px;
				
				.other-content_item{
					width: 30px;
					height: 30px;
					overflow: hidden;
					box-sizing: border-box;
					border: 1px solid #ccc;
					display: flex;
					justify-content: center;
					align-items: center;
					margin: 10px 10px;
					border-radius: 50%;
					
					
					image{
						width: 25px;
						height: 25px;
						overflow: hidden;
						box-sizing: border-box;
					}
				}
			}
		}
	}
</style>
