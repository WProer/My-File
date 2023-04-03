<template>
	<view class="cryptography-content">
		<scroll-view class="cryptographyCont-scroll" scroll-x="true">
			<view class="cryptographyCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Network-Security/cryptography/cryptographyImageOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="cryptographyCont_Views">
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
						url:require("../../../static/Network-Security/cryptography/cryptographyImageOne.jpg"),
						CourTitle:"公钥密码学数学基础",
						CourTeacher:"山东大学——庄金成、许光午、文洁晶、胡思煌、张一炜",
						ViewPersonal:"365"
					},
					{
						url:require("../../../static/Network-Security/cryptography/cryptographyImageTwo.jpg"),
						CourTitle:"密码学引论",
						CourTeacher:"山东大学——魏普文、王美琴、王薇、张国艳、庄金成、文洁晶",
						ViewPersonal:"354"
					},
					{
						url:require("../../../static/Network-Security/cryptography/cryptographyImageThree.jpg"),
						CourTitle:"现代密码学",
						CourTeacher:"电子科技大学——聂旭云、熊虎、廖永建、陈大江、王煜宇",
						ViewPersonal:"3625"
					},
					{
						url:require("../../../static/Network-Security/cryptography/cryptographyImageFour.jpg"),
						CourTitle:"区块链中的密码学",
						CourTeacher:"陆军工程大学——徐伟光",
						ViewPersonal:"365"
					},
					{
						url:require("../../../static/Network-Security/cryptography/cryptographyImageFive.jpg"),
						CourTitle:"密码学原理",
						CourTeacher:"华中科技大学——汤学明、徐鹏、骆婷",
						ViewPersonal:"365"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.cryptography-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.cryptographyCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.cryptographyCont-scroll-item {
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
				
				.cryptographyCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
