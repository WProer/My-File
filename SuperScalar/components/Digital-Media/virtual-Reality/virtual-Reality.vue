<template>
	<view class="VirtualRea-content">
		<scroll-view class="VirtualReaCont-scroll" scroll-x="true">
			<view class="VirtualReaCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Digital-Media/virtual-Reality/virtual-RealityImgOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="VirtualReaCont_Views">
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
						url:require("../../../static/Digital-Media/virtual-Reality/virtual-RealityImgOne.jpg"),
						CourTitle:"数字图像处理",
						CourTeacher:"武汉理工大学——黄朝兵、杨杰、郭志强",
						ViewPersonal:"36548"
					},
					{
						url:require("../../../static/Digital-Media/virtual-Reality/virtual-RealityImgTwo.jpg"),
						CourTitle:"数字营销：走进智慧的品牌",
						CourTeacher:"暨南大学——谷虹",
						ViewPersonal:"3654"
					},
					{
						url:require("../../../static/Digital-Media/virtual-Reality/virtual-RealityImgThree.jpg"),
						CourTitle:"虚拟现实原理与实践",
						CourTeacher:"中国传媒大学——黄心渊",
						ViewPersonal:"36524"
					},
					{
						url:require("../../../static/Digital-Media/virtual-Reality/virtual-RealityImgFour.jpg"),
						CourTitle:"沉浸式媒体：虚拟现实、增强现实与混合现实",
						CourTeacher:"中国科学技术大学——张燕翔",
						ViewPersonal:"325"
					},
					{
						url:require("../../../static/Digital-Media/virtual-Reality/virtual-RealityImgFive.jpg"),
						CourTitle:"灵境——虚拟现实技术的应用",
						CourTeacher:"南京大学——金莹",
						ViewPersonal:"3325"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.VirtualRea-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.VirtualReaCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.VirtualReaCont-scroll-item {
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
				
				.VirtualReaCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
