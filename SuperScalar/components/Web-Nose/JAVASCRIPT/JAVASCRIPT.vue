<template>
	<view class="JAVASCRIPT-Content">
		<scroll-view class="JAVASCRIPT-scroll" scroll-x="true">
			<view class="JAVASCRIPT-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Web-Nose/JAVASCRIPT/IMAGE.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="JAVASCRIPT_Views">
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
						url:require("../../../static/Web-Nose/JAVASCRIPT/IMAGE.jpg"),
						CourTitle:"JavaScript及框架应用",
						CourTeacher:"江苏电子信息职业学院，郑丽萍",
						ViewPersonal:"1481"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.JAVASCRIPT-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.JAVASCRIPT-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.JAVASCRIPT-scroll-item {
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
				
				.JAVASCRIPT_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
