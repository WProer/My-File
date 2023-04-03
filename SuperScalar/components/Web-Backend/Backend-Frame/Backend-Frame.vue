<template>
	<view class="BackendFrame-Content">
		<scroll-view class="BackendFrame-scroll" scroll-x="true">
			<view class="BackendFrame-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/WebBackend/BackendFrame/BackendFrame-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="BackendFrame_Views">
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
						url:require("../../../static/WebBackend/BackendFrame/BackendFrame-one.jpg"),
						CourTitle:" Web框架技术",
						CourTeacher:"郑州轻工业大学——张志峰、马军霞、谷培培、赵晓君、韩朴杰、李玉华、师夏阳、桑永宣、黄艳、刘育熙",
						ViewPersonal:"46548"
					},
					{
						url:require("../../../static/WebBackend/BackendFrame/BackendFrame-two.jpg"),
						CourTitle:"JavaScript及框架应用",
						CourTeacher:"江苏电子信息职业学院——郑丽萍",
						ViewPersonal:"13248"
					},
					{
						url:require("../../../static/WebBackend/BackendFrame/BackendFrame-three.png"),
						CourTitle:"Angular Web前端框架开发基础",
						CourTeacher:"北方工业大学",
						ViewPersonal:"1348"
					},
					{
						url:require("../../../static/WebBackend/BackendFrame/BackendFrame-four.jpg"),
						CourTitle:"移动互联工程实训——商城框架及首页",
						CourTeacher:"淄博职业学院——王倩",
						ViewPersonal:"830744"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.BackendFrame-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.BackendFrame-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.BackendFrame-scroll-item {
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
				
				.BackendFrame_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
