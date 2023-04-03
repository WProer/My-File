<template>
	<view class="MobileDeve">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="MobileDeve_item">
				<text>ios原生系统开发<text>_______</text> <text>推荐课程</text></text>
				<view class="MobileDevelopment_item">
					<ios-system></ios-system>
				</view>
			</view>
			<view class="MobileDeve_item">
				<text>安卓原生APP开发<text>_______</text> <text>推荐课程</text></text>
				<view class="MobileDevelopment_item">
					<AndroidSystem></AndroidSystem>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import iosSystem from "./iosSystem/iosSystem.vue"
	
	import AndroidSystem from "./AndroidSystem/AndroidSystem.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			iosSystem,
			AndroidSystem
		}
	}
</script>

<style lang="scss">
	.MobileDeve {
		height: 100%;
		display: flex;
		flex-direction: column;
		flex: 1;
		overflow: hidden;
		box-sizing: border-box;
		padding: 0px 5px;

		.scroll-list {
			height: 100%;
			display: flex;
			flex: 1;
			flex-direction: column;

			.MobileDeve_item {
				height: 60%;
				border: 1px solid #00ffff;
				background-color: #fff;
				overflow: hidden;
				box-sizing: border-box;
				padding: 5px 10px;
				border-radius: 10px;
				margin-bottom: 10px;

				text {
					width: 100%;
					font-size: 25px;
					color: #aaaaff;
					font-weight: 700;
					
					text{
						font-size: 15px;
					}
				}

				.MobileDevelopment_item {
					height: 100%;
					width: 100%;
					overflow: hidden;
					box-sizing: border-box;
				}
			}
		}
	}
</style>
