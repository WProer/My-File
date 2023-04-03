<template>
	<view class="Computer-Grade-Certificate">
		
		<scroll-view class="scroll-list" scroll-y="true" >
			<view class="Computer-Certificate_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Certificate_item" style="border: none; height: auto;">
						<text>计算机一级 <text>_______</text> <text>知识点练习</text></text>
						<ComputerLevelOne></ComputerLevelOne>
					</view>
				</scroll-view>
			</view>
			<view class="Computer-Certificate_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Certificate_item" style="border: none; height: auto;">
						<text>计算机二级 <text>_______</text> <text>知识点练习</text></text>
						<ComputerLevelTwo></ComputerLevelTwo>
					</view>
				</scroll-view>
			</view>
			<view class="Computer-Certificate_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Certificate_item" style="border: none; height: auto;">
						<text>计算机三级 <text>_______</text> <text>知识点练习</text></text>
						<ComputerLevelThree></ComputerLevelThree>
					</view>
				</scroll-view>
			</view>
			<view class="Computer-Certificate_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Certificate_item" style="border: none; height: auto;">
						<text>计算机四级 <text>_______</text> <text>知识点练习</text></text>
						<ComputerLevelFour></ComputerLevelFour>
					</view>
				</scroll-view>
			</view>
		</scroll-view>
		
		
	</view>
</template>

<script>
	import ComputerLevelOne from "./Computer-levelOne/Computer-levelOne.vue"
	import ComputerLevelTwo from "./Computer-levelTwo/Computer-levelTwo.vue"
	import ComputerLevelThree from "./Computer-levelThree/Computer-levelThree.vue"
	import ComputerLevelFour from "./Computer-levelFour/Computer-levelFour.vue"
	export default {
		name:"Computer-Grade-Certificate",
		data() {
			return {
				
			};
		},
		components:{
			ComputerLevelOne,
			ComputerLevelTwo,
			ComputerLevelThree,
			ComputerLevelFour
		}
	}
</script>

<style lang="scss">
	.Computer-Grade-Certificate{
		height: 100%;
		display: flex;
		flex-direction: column;
		flex: 1;
		overflow: hidden;
		box-sizing: border-box;
		padding: 0px 5px;
		
		.scroll-list{
			height: 100%;
			margin-top: 10px;
			display: flex;
			flex: 1;
			flex-direction: column;
			overflow: hidden;
			box-sizing: border-box;
			
			.Computer-Certificate_item{
				height: 300px;
				background-color: #f1f1ff;
				border: 1px solid #00ffff;
				border-radius: 10px;
				overflow: hidden;
				box-sizing: border-box;
				padding: 5px 10px;
				margin-bottom: 10px;
				
				text{
					width: 100%;
					font-size: 15px;
					color: #aaaaff;
					font-weight: 700;
					
					text{
						font-size: 10px;
					}
				}
			}
		}
	}

</style>