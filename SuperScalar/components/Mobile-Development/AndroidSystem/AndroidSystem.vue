<template>
	<view class="AndroidSystem-Content">
		<scroll-view class="AndroidSystem-scroll" scroll-x="true">
			<view class="AndroidSystem-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-one.png"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="AndroidSystem_Views">
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
						url:require("../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-one.png"),
						CourTitle:"App Inventor-零基础Android移动应用开发",
						CourTeacher:"浙大城市学院——吴明辉、颜晖、朱凡微、郑贝佳",
						ViewPersonal:"16548"
					},
					{
						url:require("../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-two.jpg"),
						CourTitle:"Android应用开发",
						CourTeacher:"苏州市职业大学——罗伟、戴桂平、彭学仕、胡志峰",
						ViewPersonal:"125468"
					},
					{
						url:require("../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-three.jpg"),
						CourTitle:"Android 移动应用开发",
						CourTeacher:"南宁职业技术学院 ——段仕浩、黄伟、徐冬、苏叶健、毛华彬、黄羽新、王夏林",
						ViewPersonal:"56856"
					},
					{
						url:require("../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-four.jpg"),
						CourTitle:"移动APP开发基础",
						CourTeacher:"常州信息职业技术学院——解志君 、余永佳、顾婷、刘燕婷、周伟、罗达晖、陆焱、靳霖",
						ViewPersonal:"830744"
					},
					{
						url:require("../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-five.png"),
						CourTitle:"Android开发",
						CourTeacher:"陕西国防工业职业技术学院——刘慧梅、张巍然、丁黎明",
						ViewPersonal:"3644"
					},
					{
						url:require("../../../static/MobileDevelopment/AndroidApp/iOSSystemImg-six.jpg"),
						CourTitle:"App Inventor移动应用开发",
						CourTeacher:"湖南师范大学——瞿绍军、代建华、罗迅",
						ViewPersonal:"69995"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.AndroidSystem-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.AndroidSystem-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.AndroidSystem-scroll-item {
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
				
				.AndroidSystem_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
