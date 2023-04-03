<template>
	<view class="ComputerGraphics-Content">
		<scroll-view class="ComputerGraphics-scroll" scroll-x="true">
			<view class="ComputerGraphics-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/GameDevelopment/ComputerGraphics/ComputerGraphicsImg-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="ComputerGraphics_Views">
					<uni-icons type="person"></uni-icons>
					<text style="color: #7a7a7a;">{{item.ViewPersonal}}</text>
				</view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				CourData:[
					{
						url:require("../../../static/GameDevelopment/ComputerGraphics/ComputerGraphicsImg-one.jpg"),
						CourTitle:"计算机图形学",
						CourTeacher:"中国农业大学，赵明",
						ViewPersonal:"16548"
					},
					{
						url:require("../../../static/GameDevelopment/ComputerGraphics/ComputerGraphicsImg-two.jpg"),
						CourTitle:"计算机图形学",
						CourTeacher:"华中科技大学，万琳、何云峰、陈维亚",
						ViewPersonal:"16548"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.ComputerGraphics-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.ComputerGraphics-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.ComputerGraphics-scroll-item {
				display: inline-block;
				overflow: hidden;
				box-sizing: border-box;
				width: 50%;
				height: 100%;
				margin-right: 20px;
				border: 1px solid $base-color;
				border-radius: 5px;
				white-space: nowrap;
				
				image{
					width: 100%;
					height: 90px;
				}
				
				text{
					display: block;
					text-overflow: ellipsis;
					-webkit-line-clamp: 1;
					-webkit-box-orient: vertical;
				}
				
				.ComputerGraphics_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
