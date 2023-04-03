<template>
	<view class="discuss-content">
		<scroll-view class="scroll-view" v-for="(item,index) in data" :key="index">
			<view class="discuss-content-title">
				<image :src="item.headImage"></image>
				<view class="discuss-title">
					<text>{{item.title}}</text>
					<text class="heatOne">{{item.heatOne}}</text>
					<text class="heatTwo" v-if="item.heatTwo == '热'">{{item.heatTwo}}</text>
					<text class="heatThree" v-else-if="item.heatTwo == '荐'">{{item.heatTwo}}</text>
					<text class="heatFour" v-else="item.heatTwo == '精'">{{item.heatTwo}}</text>
				</view>
			</view>
			<view class="discuss-content-item">
				<view class="discuss-item-name">
					<text>{{item.name}}</text>
					<text>发表于{{item.time}}</text>
				</view>
				<view class="discuss-item-start">
					<view class="">
						<uni-icons type="eye-filled"></uni-icons>
						<text>{{item.Views}}</text>
					</view>
					<view class="">
						<uni-icons type="chatbubble"></uni-icons>
						<text>{{item.Review}}</text>
					</view>
					<view class="">
						<uni-icons type="hand-up"></uni-icons>
						<text>{{item.Likes}}</text>
					</view>
				</view>
			</view>
		</scroll-view>
		<BackTop></BackTop>
		<discuss-edit></discuss-edit>
	</view>
</template>

<script>
	export default {
		name: "discuss-content",
		data() {
			return {
				data: [{
						headImage: "../../static/head-portrait1.jpg",
						title: "自学计算机怎样找IT工作？",
						heatOne: "顶",
						heatTwo: "热",
						name: "Hania",
						time: "[2022-10-12 09:49]",
						Views: "1236",
						Review: "35",
						Likes: "588"
					},
					{
						headImage: "../../static/head-portrait2.jpg",
						title: "java方向的话是考研还是直接参加工作？",
						heatOne: "顶",
						heatTwo: "荐",
						name: "Admin-Clark",
						time: "[2022-06-10 16:02]",
						Views: "3599",
						Review: "158",
						Likes: "4588"
					},
					{
						headImage: "../../static/head-portrait3.jpg",
						title: "为什么少有看见讨论Python的岗位？",
						heatOne: "顶",
						heatTwo: "精",
						name: "Admin-nico",
						time: "[2022-05-18 15:12]",
						Views: "2548",
						Review: "568",
						Likes: "488"
					},
					{
						headImage: "../../static/head-portrait4.jpg",
						title: "算法工程师",
						heatOne: "顶",
						heatTwo: "热",
						name: "Admin-nigk",
						time: "[2022-11-07 11:45]",
						Views: "5479",
						Review: "985",
						Likes: "2466"
					},
					{
						headImage: "../../static/head-portrait5.jpg",
						title: "关于高级数据结构",
						heatOne: "顶",
						heatTwo: "精",
						name: "Admin-Luna",
						time: "[2022-09-10 20:10]",
						Views: "7985",
						Review: "5822",
						Likes: "4566"
					},
					{
						headImage: "../../static/head-portrait6.jpg",
						title: "面试题|Python面试算法题",
						heatOne: "顶",
						heatTwo: "荐",
						name: "Admin-jack",
						time: "[2022-11-05 11:03]",
						Views: "5683",
						Review: "5822",
						Likes: "5088"
					},
					{
						headImage: "../../static/head-portrait7.jpg",
						title: "C++还是Java的岗位多？",
						heatOne: "顶",
						heatTwo: "热",
						name: "andy",
						time: "[2022-11-21 16:40]",
						Views: "6858",
						Review: "687",
						Likes: "924"
					},
					{
						headImage: "../../static/head-portrait8.jpg",
						title: "CSS优先级",
						heatOne: "顶",
						heatTwo: "精",
						name: "student",
						time: "[2022-07-12 23:16]",
						Views: "1956",
						Review: "1003",
						Likes: "654"
					},
					{
						headImage: "../../static/head-portrait9.jpg",
						title: "Web想进大厂，刷题量应该达到什么级别",
						heatOne: "顶",
						heatTwo: "精",
						name: "Jerry",
						time: "[2022-08-31 10:27]",
						Views: "8956",
						Review: "3255",
						Likes: "5088"
					},
					{
						headImage: "../../static/head-portrait10.jpg",
						title: "C/C++嵌入式开发",
						heatOne: "顶",
						heatTwo: "荐",
						name: "Aquamarine",
						time: "[2022-09-14 21:52]",
						Views: "6516",
						Review: "3654",
						Likes: "3200"
					},
					{
						headImage: "../../static/head-portrait11.jpg",
						title: "量化Java数据开发工程师",
						heatOne: "顶",
						heatTwo: "热",
						name: "Stephen",
						time: "[2022-10-03 17:41]",
						Views: "3548",
						Review: "2654",
						Likes: "1522"
					},
					{
						headImage: "../../static/head-portrait12.jpg",
						title: "Python要学习什么内容来加强",
						heatOne: "顶",
						heatTwo: "荐",
						name: "Steven",
						time: "[2022-11-17 11:05]",
						Views: "6522",
						Review: "3566",
						Likes: "3558"
					}
				]
			};
		},
		
		methods:{
			
		}
	}
</script>

<style lang="scss">
	.discuss-content {
		width: 100%;
		height: 100%;
		display: flex;
		flex-wrap: wrap;
		box-sizing: border-box;

		.scroll-view {
			width: 100%;
			height: 165px;
			display: flex;
			flex-direction: column;
			border: 2px solid #b9c8ff;
			box-shadow: 1px 1px 3px 2px #b9c8ff;
			margin: 10px;
			border-radius: 5px;
			overflow: hidden;
			box-sizing: border-box;
			background-color: $base-color;

			.discuss-content-title {
				width: 100%;
				height: 70%;
				overflow: hidden;
				box-sizing: border-box;
				display: flex;

				image {
					width: 25%;
					height: 90%;
					overflow: hidden;
					box-sizing: border-box;
					margin: 10px;
				}

				.discuss-title {
					width: 70%;
					height: 90%;
					margin: 10px 0px;
					padding: 0px 10px;
					font-size: 17px;
					font-weight: 700;
					overflow: hidden;
					box-sizing: border-box;

					text {
						color: #fff;
						font-size: 20px;
						margin-right: 15px;
						overflow: hidden;
						
					}
					
					text:nth-child(1){
						text-overflow: ellipsis;
						display: -webkit-box;
						-webkit-line-clamp: 2;
						-webkit-box-orient: vertical;
					}

					.heatOne {
						background-color: orangered;
					}

					.heatTwo {
						background-color: orange;
					}

					.heatThree {
						background-color: greenyellow;
					}

					.heatFour {
						background-color: #06ff38;
					}

				}
			}

			.discuss-content-item {
				width: 100%;
				height: 30%;
				overflow: hidden;
				box-sizing: border-box;
				display: flex;
				flex-direction: column;

				.discuss-item-name {
					width: 100%;
					height: 50%;
					overflow: hidden;
					box-sizing: border-box;
					padding: 0px 15px;
					display: flex;
					justify-content: space-between;


					text {
						color: #fff;
						font-weight: 700;
						
					}
					
					text:nth-child(1){
						color: #ff684e;
					}
				}

				.discuss-item-start {
					width: 100%;
					height: 50%;
					overflow: hidden;
					box-sizing: border-box;
					padding: 0px 55px;
					display: flex;
					justify-content: space-around;

					.uni-icons {
						color: #fff !important;
						font-weight: 700 !important;
					}

					text {
						color: #fff;
						font-weight: 700;
					}
				}
			}
		}
	}
</style>
