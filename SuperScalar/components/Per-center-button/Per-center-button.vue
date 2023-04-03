<template>
	<view class="button-content">

		<view class="button-Personal_center button-setting" v-for="(item,index) in buttonInfo" :key="index"
			@click="buttonClick(index)">
			<uni-icons :type="item.icon"></uni-icons>
			<text>{{item.title}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		name: "Per-center-button",
		data() {
			return {
				buttonInfo: [
					{
						title: "基本资料",
						icon: "list"
					},
					{
						title: "提醒设置",
						icon: "notification"
					},
					{
						title: "修改密码",
						icon: "settings"
					}
				]
			};
		},

		methods: {
			buttonClick(index) {
				if(index === 0){
					uni.navigateTo({
						url: '../../pages/Personal-Center/Basic-Information/Basic-Information'
					})
				}
				else if (index === 1) {
					uni.navigateTo({
						url: '../../pages/Personal-Center/Reminder-Settings/Reminder-Settings'
					})
				}else if(index === 2){
					uni.navigateTo({
						url:'../../pages/Personal-Center/Change-Password/Change-Password'
					})
				}

			}
		}
	}
</script>

<style lang="scss">
	.button-content {
		height: 100%;
		margin-top: 20px;
		display: flex;
		justify-content: space-around;
		flex-wrap: wrap;
		padding: 10px 25px;

		.button-setting {
			flex-shrink: 0;
			width: 100%;
			height: 50px;
			border: 2px solid #3cb8b8;
			margin-top: 10px;
			overflow: hidden;
			box-sizing: border-box;
			border-radius: 10px;
			display: flex;
			justify-content: start;
			align-items: center;

			.uni-icons {
				font-size: 25px !important;
				margin-left: 10px;
				color: #FFFFFF !important;
			}

			text {
				font-size: 20px;
				color: #FFFFFF;
				margin-left: 13px;
				font-weight: 700;
			}
		}
	}
</style>
