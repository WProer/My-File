<template>
	<view class="center-record">
		<view class="record-title">
			<h3>浏览过得课程</h3>
		</view>
		<hr>
		<view class="record-Historic_records">
			<h4>暂无浏览记录</h4>
		</view>
	</view>
</template>

<script>
	export default {
		name:"Per-center_record",
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.center-record{
		height: 100%;
		margin-top: 25px;
			overflow: hidden;
			box-sizing: border-box;
		
		.record-title{
			height: 100%;
			padding: 10px 10px;
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			justify-content: center;
			align-items: center;
			color: #FFFFFF;
		}
		
		.record-Historic_records{
			height: 1000px;
			padding: 10px 10px;
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			justify-content: center;
			color: #FFFFFF;
		}
	}
</style>