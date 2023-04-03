<template>
	<view class="Digital-Media">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="Digital-Media_item">
				<text>Adobe系列 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<Adobe></Adobe>
				</view>
			</view>
			<view class="Digital-Media_item">
				<text>FFmpeg <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<FFmpeg></FFmpeg>
				</view>
			</view>
			<view class="Digital-Media_item">
				<text>3dmax与maya <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<Maya></Maya>
				</view>
			</view>
			<view class="Digital-Media_item">
				<text>虚拟现实 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<VirtualRea></VirtualRea>
				</view>

			</view>

		</scroll-view>


	</view>
</template>

<script>
	import Adobe from "./Adobe/Adobe.vue"
	import FFmpeg from "./FFmpeg/FFmpeg.vue"
	import Maya from "./maya/maya.vue"
	import VirtualRea from "./virtual-Reality/virtual-Reality.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			Adobe,
			FFmpeg,
			Maya,
			VirtualRea

		}
	}
</script>

<style lang="scss">
	.Digital-Media {
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

			.Digital-Media_item {
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
