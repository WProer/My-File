<template>
	<view class="Adobe-content">
		<scroll-view class="AdobeCont-scroll" scroll-x="true">
			<view class="AdobeCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="AdobeCont_Views">
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
						url:require("../../../static/Digital-Media/Adobe/AdobeImageOne.jpg"),
						CourTitle:"Adobe Illustrator 图形图像制作",
						CourTeacher:"武汉船舶职业技术学院——梁娜、周姗、徐佳佳、梁娜、周姗、徐佳佳",
						ViewPersonal:"12345"
					},
					{
						url:require("../../../static/Digital-Media/Adobe/AdobeImageTwo.jpg"),
						CourTitle:"Adobe大师教程系列",
						CourTeacher:"Adobe奥多比官方",
						ViewPersonal:"246"
					},
					{
						url:require("../../../static/Digital-Media/Adobe/AdobeImageThree.jpg"),
						CourTitle:"Adobe产品新功能系列",
						CourTeacher:"Adobe奥多比官方",
						ViewPersonal:"1368"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Adobe-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.AdobeCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.AdobeCont-scroll-item {
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
				
				.AdobeCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
