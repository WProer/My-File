<template>
	<view class="Progress-Area_content">
		<view class="Learning-ProgressBar">
			<view class="Learning-ProgressBar_content">
			</view>
			<view class="Learning-ProgressBar_Rate">
				正确率：<text>0%</text>
			</view>
		</view>
		<view class="Number-questions">
			<text>0 / 0 / 102 (已做/未做/总数)</text>
			<button>开始练习</button>
		</view>
		
	</view>
</template>

<script>
	export default {
		name: "Progress-Area",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	
	.Progress-Area_content{
		overflow: hidden;
		box-sizing: border-box;
		
		view{
			height: 30px;
		}
		.Learning-ProgressBar {
			display: flex;
			justify-content: space-between;
			overflow: hidden;
			box-sizing: border-box;
		
			.Learning-ProgressBar_content {
				width: 200px;
				height: 20px;
				background-color: #e2e2e2;
				border-radius: 15px;
				padding: 0px 5px;
				overflow: hidden;
				box-sizing: border-box;
				margin-top: 5px;
			}
		
			.Learning-ProgressBar_Rate {
				width: 100px;
				margin-top: 5px;
		
				text {
					color: red;
				}
			}
		}
		
		.Number-questions {
			display: flex;
			justify-content: space-between;
			align-items: center;
			overflow: hidden;
			box-sizing: border-box;
			color: #ccc;
			justify-content: space-between;
		
			button {
				margin: 0px;
				font-size: 10px;
				border: 1px solid $base-color;
				background-color: #fff;
				border-radius: 15px;
			}
		}
	}
	
</style>
