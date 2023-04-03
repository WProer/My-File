<template>
	<view class="PythonLanguage-content">
		<scroll-view class="PythonLanguageCont-scroll" scroll-x="true">
			<view class="PythonLanguageCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Artificial-Intelligence/Python/PythonImageOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="PythonLanguageCont_Views">
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
						url:require("../../../static/Artificial-Intelligence/Python/PythonImageOne.jpg"),
						CourTitle:"Python语言程序设计",
						CourTeacher:"北京理工大学——嵩天、黄天羽、礼欣",
						ViewPersonal:"3625"
					},
					{
						url:require("../../../static/Artificial-Intelligence/Python/PythonImageTwo.jpg"),
						CourTitle:"python+",
						CourTeacher:"河南师范大学——张磊、张倩倩、刘金金、郭凌云、李晓艳、李志先、陶华亭、黄晓巧、王爱菊、陈劲松、夏辉丽、耿秀义、陈二浩",
						ViewPersonal:"2564"
					},
					{
						url:require("../../../static/Artificial-Intelligence/Python/PythonImageThree.jpg"),
						CourTitle:"Python数据分析-零基础速成Python",
						CourTeacher:"刘经纬",
						ViewPersonal:"36254"
					},
					{
						url:require("../../../static/Artificial-Intelligence/Python/PythonImageFour.jpg"),
						CourTitle:"Python程序设计",
						CourTeacher:"中国矿业大学——孙晋非、周勇、张瑾、高璟",
						ViewPersonal:"3654"
					},
					{
						url:require("../../../static/Artificial-Intelligence/Python/PythonImageFive.jpg"),
						CourTitle:"Python网络爬虫与信息提取",
						CourTeacher:"北京理工大学——嵩天、黄天羽",
						ViewPersonal:"3325"
					},
					{
						url:require("../../../static/Artificial-Intelligence/Python/PythonImageSix.jpg"),
						CourTitle:"Python编程基础",
						CourTeacher:"南开大学——王恺、李妍、闫晓玉、施莺莺、李涛",
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
	.PythonLanguage-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.PythonLanguageCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.PythonLanguageCont-scroll-item {
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
				
				.PythonLanguageCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
