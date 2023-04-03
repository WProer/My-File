<template>
	<view class="JAVA-Content">
		<scroll-view class="JAVA-scroll" scroll-x="true">
			<view class="JAVA-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/WebBackend/JAVA/JAVAIMG-one.png"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="JAVA_Views">
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
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-one.png"),
						CourTitle:"Java速成",
						CourTeacher:"刘经纬",
						ViewPersonal:"16548"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-two.png"),
						CourTitle:"零基础上岸Java",
						CourTeacher:"王道-深澜、王道-北海、王道-天明",
						ViewPersonal:"125468"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-three.png"),
						CourTitle:"Java程序设计",
						CourTeacher:"北京大学——唐大仕",
						ViewPersonal:"56856"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-four.jpg"),
						CourTitle:"Java Web开发基础",
						CourTeacher:"广东轻工职业技术学院——张婵、罗佳、古凌岚、罗茂权、吴绍根、陈宏扬",
						ViewPersonal:"830744"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-five.png"),
						CourTitle:"基于Java的面向对象编程范式",
						CourTeacher:"南京大学——刘钦",
						ViewPersonal:"3644"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-six.jpg"),
						CourTitle:"Java核心技术",
						CourTeacher:"华东师范大学——陈良育",
						ViewPersonal:"69995"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-seven.png"),
						CourTitle:"Java程序设计",
						CourTeacher:"常州信息职业技术学院——杨丹、眭碧霞、蒋卫祥、张静、朱利华、闾枫、杜伟、陶艺文",
						ViewPersonal:"141"
					},
					{
						url:require("../../../static/WebBackend/JAVA/JAVAIMG-eight.jpeg"),
						CourTitle:"JAVA语言程序设计",
						CourTeacher:"南京邮电大学——杨建",
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
	.JAVA-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.JAVA-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.JAVA-scroll-item {
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
				
				.JAVA_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
