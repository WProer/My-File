<template>
	<view class="ThreeGameDeve-Content">
		<scroll-view class="ThreeGameDeve-scroll" scroll-x="true">
			<view class="ThreeGameDeve-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="ThreeGameDeve_Views">
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
						url:require("../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-one.jpg"),
						CourTitle:"3D动画与特效",
						CourTeacher:"中国科学技术大学，张燕翔",
						ViewPersonal:"56811"
					},
					{
						url:require("../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-two.jpg"),
						CourTitle:"游戏引擎原理及应用",
						CourTeacher:"中国传媒大学，韩红雷",
						ViewPersonal:"125468"
					},
					{
						url:require("../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-three.jpg"),
						CourTitle:"游戏策划",
						CourTeacher:"上海戏剧学院，朱云",
						ViewPersonal:"56856"
					},
					{
						url:require("../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-four.png"),
						CourTitle:"3D设计软件应用",
						CourTeacher:"福建工程学院，伊启中",
						ViewPersonal:"4564"
					},
					{
						url:require("../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-five.jpg"),
						CourTitle:"游戏开发程序设计基础",
						CourTeacher:"中国传媒大学，韩红雷",
						ViewPersonal:"3644"
					},
					{
						url:require("../../../static/GameDevelopment/3DGameDeve/3DGameDeveImg-six.jpg"),
						CourTitle:"游戏设计原理",
						CourTeacher:"中国地质大学，桂宇晖",
						ViewPersonal:"66598"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.ThreeGameDeve-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.ThreeGameDeve-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.ThreeGameDeve-scroll-item {
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
				
				.ThreeGameDeve_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
