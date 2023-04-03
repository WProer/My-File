<template>
	<view class="Computer-Software-Test">
		
		<scroll-view class="scroll-list" scroll-y="true" >
			<view class="Computer-Software_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Software_item" style="border: none; height: auto;">
						<text>初级 <text>_______</text> <text>知识点练习</text></text>
						<SoftBeginner></SoftBeginner>
					</view>
				</scroll-view>
			</view>
			<view class="Computer-Software_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Software_item" style="border: none; height: auto;">
						<text>中级 <text>_______</text> <text>知识点练习</text></text>
						<IntermediateSoft></IntermediateSoft>
					</view>
				</scroll-view>
			</view>
			<view class="Computer-Software_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Computer-Software_item" style="border: none; height: auto;">
						<text>高级 <text>_______</text> <text>知识点练习</text></text>
						<AdvancedSoft></AdvancedSoft>
					</view>
				</scroll-view>
			</view>
		</scroll-view>
		
		
	</view>
</template>

<script>
	import SoftBeginner from "./Soft-Exam-Beginner/Soft-Exam-Beginner.vue"
	import IntermediateSoft from "./Intermediate-Soft-Test/Intermediate-Soft-Test.vue"
	import AdvancedSoft from "./Advanced-Soft-Test/Advanced-Soft-Test.vue"
	export default {
		name:"Computer-Software-Test",
		data() {
			return {
				
			};
		},
		components:{
			SoftBeginner,
			IntermediateSoft,
			AdvancedSoft
		}
	}
</script>

<style lang="scss">
	.Computer-Software-Test{
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
			
			.Computer-Software_item{
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