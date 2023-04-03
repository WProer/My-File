<template>
	<view class="Web-Backend">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="Web-Backend_item">
				<text>JAVA <text>_______</text> <text>推荐课程</text></text>
				<view class="JAVA_item">
					<JAVACON></JAVACON>
				</view>
			</view>
			<view class="Web-Backend_item">
				<text>操作系统与计算机网络 <text>_______</text> <text>推荐课程</text></text>
				<view class="JAVA_item">
					<OperatingSystem></OperatingSystem>
				</view>
			</view>
			<view class="Web-Backend_item">
				<text>后端框架 <text>_______</text> <text>推荐课程</text></text>
				<view class="JAVA_item">
					<BackendFrame></BackendFrame>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import JAVACON from "./Java-Content/Java-Content.vue"
	
	import OperatingSystem from "./Operating-System/Operating-System.vue"
	
	import BackendFrame from "./Backend-Frame/Backend-Frame.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			JAVACON,
			OperatingSystem,
			BackendFrame
		}
	}
</script>

<style lang="scss">
	.Web-Backend {
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

			.Web-Backend_item {
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

				.JAVA_item {
					height: 100%;
					width: 100%;
					overflow: hidden;
					box-sizing: border-box;
				}
			}
		}
	}
</style>
