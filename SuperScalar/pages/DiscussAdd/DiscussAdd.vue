<template>
	<view class="DiscussAdd-Content">
		<view class="DiscussAdd-content_Menu">
			<text>新讨论</text>
			<view class="DiscussAdd-Menu_Content">
				<button>发表</button>
				<button>定时发表</button>
				<button>存草稿</button>
				<button @click="BackPage()">关闭</button>
			</view>
		</view>
		
		<view class="DiscussAdd-content_Area">
			
			<view class="DiscussAdd-Area_Title">
				<text>标题</text><input type="text" placeholder="请输入标题">
			</view>
			
			<view class="DiscussAdd-Area_TEXT">
				<text>正文:</text>
				<textarea name="" id="" cols="30" rows="70"></textarea>
			</view>
			
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			BackPage(){
				uni.navigateBack({
					delta:1
				})
			}
		}
	}
</script>

<style lang="scss">
	.DiscussAdd-Content{
		width: 99%;
		height: 100vh;
		box-sizing: border-box;
		overflow: hidden;
		padding: 10px 5px;
		border: 5px solid $base-color;
		margin-left: 2px;
		.DiscussAdd-content_Menu{
			display: flex;
			flex-direction: column;
			box-sizing: border-box;
			overflow: hidden;
			border-bottom:1px solid #fff;
			
			
			text{
				width: 80px;
				height: 30px;
				display: flex;
				justify-content: center;
				align-items: center;
				background-color: $base-color;
				color: #fff;
				border: 1px solid $base-color;
				border-radius: 5px 5px 0px 0px;
				font-weight: 700;
			}
			
			.DiscussAdd-Menu_Content{
				height: 70px;
				display: flex;
				justify-content: start;
				align-items: center;
				background-color: $base-color;
				border: 1px solid $base-color;
				
				button{
					height: 40%;
					margin: 0px;
					margin-left: 3px;
					display: flex;
					align-items: center;
				}
			}
		}
		
		.DiscussAdd-content_Area{
			height: 90%;
			box-sizing: border-box;
			overflow: hidden;
			background-color: #e5e5ff;
			border-top: 1px solid skyblue;
			padding: 10px 10px;
			
			.DiscussAdd-Area_Title{
				box-sizing: border-box;
				overflow: hidden;
				display: flex;
				align-items: center;
				
				text{
					font-size: 18px;
				}
				
				input{
					width: 80%;
					height: 25%;
					border: 1px solid black;
					background-color: #fff;
					box-shadow: 0px 1px 1px 1px #ccc inset;
					margin-left: 20px;
					padding: 1px 5px;
					box-sizing: border-box;
					overflow: hidden;
					border-radius: 3px;
				}
			}
			
			.DiscussAdd-Area_TEXT{
				box-sizing: border-box;
				overflow: hidden;
				margin-top: 10px;
				
				text{
					font-size: 18px;
				}
				
				
				textarea{
					width: 99%;
					height: 500px;
					border: 1px solid black;
					overflow: hidden;
					box-sizing: border-box;
					background-color: #fff;
					border-radius: 5px;
					font-size: 15px;
				}
			}
		}
	}
</style>
