<template>
	<view class="iosSystme-Content">
		<scroll-view class="iosSystme-scroll" scroll-x="true">
			<view class="iosSystme-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/MobileDevelopment/iOSSystem/iOSSystem.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="iosSystme_Views">
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
						url:require("../../../static/MobileDevelopment/iOSSystem/iOSSystem.jpg"),
						CourTitle:"ios开发技术",
						CourTeacher:"苏州市职业大学——牛丽、尚鲜连、张量、熊志勇、李爱军",
						ViewPersonal:"28595"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.iosSystme-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.iosSystme-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.iosSystme-scroll-item {
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
				
				.iosSystme_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
