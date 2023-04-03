<template>
	<view class="Web-Nose">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="Web-Nose_item">
				<text>HTML、CSS <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<HTMLCSS></HTMLCSS>
				</view>
			</view>
			<view class="Web-Nose_item">
				<text>JavaScript <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<JAVASCRIPT></JAVASCRIPT>
				</view>
			</view>
			<view class="Web-Nose_item">
				<text>React <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<REACTFramework></REACTFramework>
				</view>
			</view>
			<view class="Web-Nose_item">
				<text>Vue <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<VUEFramework></VUEFramework>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import HTMLCSS from "./HTMLCSS/HTMLCSS.vue"
	import JAVASCRIPT from "./JAVASCRIPT/JAVASCRIPT.vue"
	import REACTFramework from "./React-Framework/React-Framework.vue"
	import VUEFramework from "./Vue-Framework/Vue-Framework.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			HTMLCSS,
			JAVASCRIPT,
			REACTFramework,
			VUEFramework
		}
	}
</script>

<style lang="scss">
	.Web-Nose {
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

			.Web-Nose_item {
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
