<template>
	<view class="ObjectOriented-Content">
		<scroll-view class="ObjectOriented-scroll" scroll-x="true">
			<view class="ObjectOriented-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Object-Oriented/Object-OrientedImg-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="ObjectOriented_Views">
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
						url:require("../../../static/Object-Oriented/Object-OrientedImg-one.jpg"),
						CourTitle:"面向对象程序设计",
						CourTeacher:"濮阳职业技术学院，李静，仇丹丹，刘琰",
						ViewPersonal:"1984"
					},
					{
						url:require("../../../static/Object-Oriented/Object-OrientedImg-two.jpg"),
						CourTitle:"面向对象程序设计",
						CourTeacher:"江苏大学，潘雨青，耿霞，郑文怡",
						ViewPersonal:"103"
					},
					{
						url:require("../../../static/Object-Oriented/Object-OrientedImg-three.jpg"),
						CourTitle:"面向对象程序设计（C++）",
						CourTeacher:"东北大学——董晓梅，张天成，谷峪，信俊昌，赵宁海，薛雨芳，徐彬",
						ViewPersonal:"671"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.ObjectOriented-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.ObjectOriented-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.ObjectOriented-scroll-item {
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
				
				.ObjectOriented_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
