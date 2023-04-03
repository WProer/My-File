<template>
	<view class="OpenCV-content">
		<scroll-view class="OpenCVCont-scroll" scroll-x="true">
			<view class="OpenCVCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Artificial-Intelligence/OpenCV/OpenCVImageOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="OpenCVCont_Views">
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
						url:require("../../../static/Artificial-Intelligence/OpenCV/OpenCVImageOne.jpg"),
						CourTitle:"机器视觉技术与应用",
						CourTeacher:"杭州电子科技大学——李竹、石振、严丽平",
						ViewPersonal:"3568"
					},
					{
						url:require("../../../static/Artificial-Intelligence/OpenCV/OpenCVImageTwo.jpg"),
						CourTitle:"Python机器学习——解“码”人工智能",
						CourTeacher:"华东师范大学——刘艳、孙仕亮、刘小平、陈宇浩",
						ViewPersonal:"1254"
					},
					{
						url:require("../../../static/Artificial-Intelligence/OpenCV/OpenCVImageThree.jpg"),
						CourTitle:"机器视觉与边缘计算应用",
						CourTeacher:"复旦大学——赵卫东、董亮",
						ViewPersonal:"365"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.OpenCV-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.OpenCVCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.OpenCVCont-scroll-item {
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
				
				.OpenCVCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
