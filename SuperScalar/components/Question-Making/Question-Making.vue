<template>
	<view class="Question-Making">	<!-- 做题记录 -->
		
		<view class="Question-Making-content">
			<view class="Question-Making_item">
				<uni-icons customPrefix="iconfont" type="icon-zuotijilu" size="35" color="#9c9c9c"></uni-icons>
				<text>做题记录</text>
			</view>
			<view class="Question-Making_item">
				<text style="margin-top: 10px;">0</text>
				<text style="margin-top: 13px;">我的错题</text>
			</view>
 			<view class="Question-Making_item">
				<text style="margin-top: 10px;">0</text>
				<text style="margin-top: 13px;">我的收藏</text>
			</view><view class="Question-Making_item">
				<text style="margin-top: 10px;">0</text>
				<text style="margin-top: 13px;">我的笔记</text>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		name:"Question-Making",
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	@import '../../static/iconfont.css';
.Question-Making{
	display: flex;
	overflow: hidden;
	box-sizing: border-box;
	padding: 10px 20px;
	
	.Question-Making-content{
		width: 100%;
		border: 1px solid #fff;
		border-radius: 5px;
		overflow: hidden;
		box-sizing: border-box;
		display: flex;
		justify-content: space-around;		
		background-color: #e5e5ff;
		box-shadow: 5px 4px 6px 1px #9c9c9c;
		
		.Question-Making_item{
			display: flex;
			flex-direction: column;
			margin: 10px 0px;
			overflow: hidden;
			box-sizing: border-box;
			
			text{
				margin: 5px 0px;
				font-weight: 700;
				color: #9c9c9c;
				text-align: center;
			}
		}
	}
}
</style>