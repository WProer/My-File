<template>
	<view class="GameDeve">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="GameDeve_item">
				<text>3D游戏开发 <text>_______</text> <text>推荐课程</text></text>
				<view class="GameDevelopment_item">
					<ThreeGameDeve></ThreeGameDeve>
				</view>
			</view>
			<view class="GameDeve_item">
				<text>2D游戏开发 <text>_______</text> <text>推荐课程</text></text>
				<view class="GameDevelopment_item">
					<TwoGameDeve></TwoGameDeve>
				</view>
			</view>
			<view class="GameDeve_item">
				<text>计算机图形学 <text>_______</text> <text>推荐课程</text></text>
				<view class="GameDevelopment_item">
					<ComputerGraphics></ComputerGraphics>
				</view>
			</view>
			<view class="GameDeve_item">
				<text>shader <text>_______</text> <text>推荐课程</text></text>
				<view class="GameDevelopment_item">
					<Shader></Shader>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import ThreeGameDeve from "./3DGameDeve/3DGameDeve.vue"
	import TwoGameDeve from "./2DGameDeve/2DGameDeve.vue"
	import ComputerGraphics from "./ComputerGraphics/ComputerGraphics.vue"
	import Shader from "./Shader/Shader.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			ThreeGameDeve,
			TwoGameDeve,
			ComputerGraphics,
			Shader
		}
	}
</script>

<style lang="scss">
	.GameDeve {
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

			.GameDeve_item {
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

				.GameDevelopment_item {
					height: 100%;
					width: 100%;
					overflow: hidden;
					box-sizing: border-box;
				}
			}
		}
	}
</style>
