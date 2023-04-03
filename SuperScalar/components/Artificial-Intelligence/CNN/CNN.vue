<template>
	<view class="CNN-content">
		<scroll-view class="CNNCont-scroll" scroll-x="true">
			<view class="CNNCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Artificial-Intelligence/CNN/CNNImageOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="CNNCont_Views">
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
						url:require("../../../static/Artificial-Intelligence/CNN/CNNImageOne.jpg"),
						CourTitle:"深度学习应用开发-TensorFlow实践",
						CourTeacher:"浙大城市学院——吴明晖、李卓蓉、金苍宏",
						ViewPersonal:"2354"
					},
					{
						url:require("../../../static/Artificial-Intelligence/CNN/CNNImageTwo.jpg"),
						CourTitle:"机器视觉与边缘计算应用",
						CourTeacher:"复旦大学——赵卫东、董亮",
						ViewPersonal:"4568"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.CNN-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.CNNCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.CNNCont-scroll-item {
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
				
				.CNNCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
