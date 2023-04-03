<template>
	<view class="TwoGameDeve-Content">
		<scroll-view class="TwoGameDeve-scroll" scroll-x="true">
			<view class="TwoGameDeve-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/GameDevelopment/2DGameDeve/2DGameDeve.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="TwoGameDeve_Views">
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
						url:require("../../../static/GameDevelopment/2DGameDeve/2DGameDeve.jpg"),
						CourTitle:"Unity 2D 游戏程序设计",
						CourTeacher:"南京信息职业技术学院 ，王晖 、解银玲、王腾",
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
	.TwoGameDeve-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.TwoGameDeve-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.TwoGameDeve-scroll-item {
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
				
				.TwoGameDeve_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
