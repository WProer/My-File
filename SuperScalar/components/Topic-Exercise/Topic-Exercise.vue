<template>
	<view class="Topic-Exercise">

		<view class="Topic-Exercise-content">
			<view class="Topic-Exercise_item">
				<uni-icons customPrefix="iconfont" type="icon-meiriyilian" size="35" color="#9c9c9c"></uni-icons>
				<text>每日一练</text>
			</view>
			<view class="Topic-Exercise_item">
				<uni-icons customPrefix="iconfont" type="icon-shijuan1" size="35" color="#9c9c9c"></uni-icons>
				<text>历年真题</text>
			</view>
			<view class="Topic-Exercise_item">
				<uni-icons customPrefix="iconfont" type="icon-shijuan" size="35" color="#9c9c9c"></uni-icons>
				<text>模拟考卷</text>
			</view>
		</view>


	</view>
</template>

<script>
	export default {
		name: "Topic-Exercise",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	@import '../../static/iconfont.css';
	.Topic-Exercise {
		display: flex;
		overflow: hidden;
		box-sizing: border-box;
		padding: 10px 20px;

		.Topic-Exercise-content {
			width: 100%;
			border: 1px solid #fff;
			border-radius: 5px;
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			justify-content: space-around;		
			background-color: #e5e5ff;
			box-shadow: 5px 4px 6px 1px #9c9c9c;
			
			.Topic-Exercise_item{
				display: flex;
				flex-direction: column;
				margin: 10px 0px;
				overflow: hidden;
				box-sizing: border-box;
				
				text{
					margin: 5px 0px;
					font-weight: 700;
					color: #9c9c9c;
				}
			}
			
		}
	}
</style>
