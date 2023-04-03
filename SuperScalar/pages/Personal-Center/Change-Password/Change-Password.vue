<template>
	<view class="Change-Password">
		<form action="">
			<view class="Change-Password_content">
				<view class="Change-Password_Item"> <text>旧密码：</text><input type="password" name="" id=""> </view>
				<view class="Change-Password_Item"> <text>新密码：</text><input type="password" name="" id=""></view>
				<view class="Change-Password_Item"> <text>确认新密码：</text><input type="password" name="" id=""> </view>
			</view>
			<view class="Password-Submit">
				<button @click="SubPassWord()">提交</button>
			</view>

		</form>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			SubPassWord() {
				uni.showToast({
					icon:'success',
					title:"修改成功！",
					duration:2000
				})
			}
		}
	}
</script>

<style lang="scss">
	.Change-Password {
		padding: 50px 30px;
		display: flex;
		flex-direction: column;

		.Change-Password_Item {
			overflow: hidden;
			box-sizing: border-box;
			// border-bottom: 1px solid #ccc;
			margin: 30px 0px;
			padding: 10px 0px;
			display: flex;

			text {
				width: 35%;
				text-align: right;
			}

			input {
				border: 1px solid #ccc;
				border-radius: 5px;
				width: 60%;
			}
		}

		button {
			background-color: $base-color;
		}


	}
</style>
