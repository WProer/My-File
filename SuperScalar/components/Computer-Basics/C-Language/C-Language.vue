<template>
	<view class="C-Language-content">
		<scroll-view class="CLang-scroll" scroll-x="true">
			<view class="CLang-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/CLanguage-two.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="CLang_Views">
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
						url:require("../../../static/CLanguage-one.jpg"),
						CourTitle:"C语言程序设计",
						CourTeacher:"浙江大学—翁凯",
						ViewPersonal:"830744"
					},
					{
						url:require("../../../static/CLanguage-two.jpg"),
						CourTitle:"程序设计入门——C语言",
						CourTeacher:"浙江大学—翁凯",
						ViewPersonal:"244656"
					},
					{
						url:require("../../../static/CLanguage-three.jpg"),
						CourTitle:"零基础学C语言",
						CourTeacher:"中国地质大学（武汉）—戴光明、马钊",
						ViewPersonal:"19656"
					},
					{
						url:require("../../../static/CLanguage-four.jpg"),
						CourTitle:"高级C语言程序设计",
						CourTeacher:"郑州师范学院—曹志娟、李华英、李焕勤、刑昀、魏萌",
						ViewPersonal:"830744"
					},
					{
						url:require("../../../static/CLanguage-five.jpg"),
						CourTitle:"C程序设计基础",
						CourTeacher:"厦门大学—黄洪艺、李慧琪、张丽丽、曾华琳、庄朝晖",
						ViewPersonal:"3644"
					},
					{
						url:require("../../../static/CLanguage-six.jpg"),
						CourTitle:"C语言程序设计——快速入门与提高",
						CourTeacher:"中国农业大学—吕春利",
						ViewPersonal:"69995"
					},
					{
						url:require("../../../static/CLanguage-seven.png"),
						CourTitle:"C语言-期末复习资料（学霸笔记）",
						CourTeacher:"考拉学姐",
						ViewPersonal:"141"
					},
					{
						url:require("../../../static/CLanguage-eight.jpg"),
						CourTitle:"C语言程序设计CAP",
						CourTeacher:"浙江大学—翁凯",
						ViewPersonal:"73049"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.C-Language-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.CLang-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.CLang-scroll-item {
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
				
				.CLang_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
