<template>
	<view class="Computer-Basics">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="Computer-Basics_item">
				<text>C语言 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<Clang></Clang>
				</view>
			</view>
			<view class="Computer-Basics_item">
				<text>数据结构与算法 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<DataStructure></DataStructure>
				</view>
			</view>
			<view class="Computer-Basics_item">
				<text>Linux && macOS <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<Linux></Linux>
				</view>
			</view>
			<view class="Computer-Basics_item">
				<text>面向对象编程 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<ObjectOriented></ObjectOriented>
				</view>
			</view>
			<view class="Computer-Basics_item">
				<text>数据库与SQL <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<DataBank></DataBank>
				</view>
			</view>
			<view class="Computer-Basics_item">
				<text>GitHub && SVN <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<GitHub></GitHub>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import Clang from './C-Language/C-Language.vue'
	import DataStructure from "./Data-Structure/Data-Structure.vue"
	import Linux from "./Linux-MACOS/Linux-MACOS.vue"
	import ObjectOriented from "./Object-Oriented/Object-Oriented.vue"
	import DataBank from "./Data-Bank/Data-Bank.vue"
	import GitHub from "./GitHub-SVN/GitHub-SVN.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			Clang,
			DataStructure,
			Linux,
			ObjectOriented,
			DataBank,
			GitHub
		}
	}
</script>

<style lang="scss">
	.Computer-Basics {
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

			.Computer-Basics_item {
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
