<template>
	<view class="search-content">
		<view class="search-left">
			<view class="search-left_logo">
				<image src="../../static/logo.png" mode=""></image>
			</view>
			<text>晨旭网</text>
		</view>
		<view class="search-right">
			<view class="search">
				<input type="text" placeholder="search">
				<uni-icons type="search" size="20px" color="#999" @click="Search()"></uni-icons>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "index-search",
		data() {
			return {

			};
		},
		methods:{
			Search(){
				uni.showToast({
					icon:'error',
					title:"无搜索内容",
					duration:2000
				})
				console.log(123);
			}
		}
	}
</script>

<style lang="scss">
	.search-content {
		width: 100%;
		height: 110%;
		overflow: hidden;
		box-sizing: border-box;
		padding: 5px 10px;
		display: flex;
		justify-content: space-around;
		align-items: center;
		border-bottom: 2px solid #3399CC;
		box-shadow: 0px 2px 2px #FFFFFF;
		
		// &::after{
		// 	content: "";
		// 	width: 100%;
		// 	height: 2px;
		// 	background-color: #fff;
		// 	position: absolute;
		// 	top: 68px;
		// 	left: 0px;
		// }

		.search-left {
			width: 50%;
			height: 100%;
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			align-items: center;
			justify-content: start;

			.search-left_logo {
				height: 100%;
				width: 50%;
				overflow: hidden;
				box-sizing: border-box;

				image {
					width: 100%;
					height: 100%;

				}
			}

			text {
				margin-left: 5px;
				color: #FFFFFF;
				font-weight: 700;
				font-size: 30px;
				text-shadow: 3px -2px 3px #9e9b9b;
			}
		}

		.search-right {
			width: 50%;
			height: 100%;
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			justify-content: end;
			align-items: center;

			.search {
				background-color: #fff;
				width: 100%;
				height: 30px;
				border-radius: 30px;
				padding: 0px 10px;
				display: flex;
				align-items: center;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
	

</style>
