<template>
	<view class="Artificial-Intelligence">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="Artificial-Intelligence_item">
				<text>Python <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<PythonLang></PythonLang>
				</view>
			</view>
			<view class="Artificial-Intelligence_item">
				<text>CNN <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<CNN></CNN>
				</view>
			</view>
			<view class="Artificial-Intelligence_item">
				<text>OpenCV <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<OpenCV></OpenCV>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import PythonLang from "./PythonLanguage/PythonLanguage.vue"
	import CNN from "./CNN/CNN.vue"
	import OpenCV from "./OpenCV/OpenCV.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			PythonLang,
			CNN,
			OpenCV
		}
	}
</script>

<style lang="scss">
	.Artificial-Intelligence {
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

			.Artificial-Intelligence_item {
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

					text {
						font-size: 15px;
					}
				}

				.C-Language_item {
					height: 100%;
					width: 100%;
					overflow: hidden;
					box-sizing: border-box;
				}
			}
		}
	}
</style>
