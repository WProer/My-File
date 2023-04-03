<template>
	<view class="Maya-content">
		<scroll-view class="MayaCont-scroll" scroll-x="true">
			<view class="MayaCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Digital-Media/3dmax-maya/mayaImageOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="MayaCont_Views">
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
						url:require("../../../static/Digital-Media/3dmax-maya/mayaImageOne.jpg"),
						CourTitle:"3DMAX环境艺术设计",
						CourTeacher:"南阳职业学院——郭荧飞、靳瑶、葛长辉",
						ViewPersonal:"2356"
					},
					{
						url:require("../../../static/Digital-Media/3dmax-maya/mayaImageTwo.jpg"),
						CourTitle:"3DMax创建之美",
						CourTeacher:"郑州信息工程职业学院——王明瑞、郭甲润",
						ViewPersonal:"136"
					},
					{
						url:require("../../../static/Digital-Media/3dmax-maya/mayaImageThree.jpg"),
						CourTitle:"室内装饰设计3DMAX应用",
						CourTeacher:"武汉交通职业学院——李爽",
						ViewPersonal:"568"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Maya-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.MayaCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.MayaCont-scroll-item {
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
				
				.MayaCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
