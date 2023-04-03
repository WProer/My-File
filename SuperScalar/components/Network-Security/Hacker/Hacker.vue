<template>
	<view class="Hacker-content">
		<scroll-view class="HackerCont-scroll" scroll-x="true">
			<view class="HackerCont-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Network-Security/Hacker/HackerImageOne.jpg" mode=""></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="HackerCont_Views">
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
						url:require("../../../static/Network-Security/Hacker/HackerImageOne.jpg"),
						CourTitle:"网络攻防技术",
						CourTeacher:"深圳信息职业技术学院 高月芳 谭旭 叶建锋 彭迎春 彭开慧 陈锦川 谢飞",
						ViewPersonal:"3625"
					},
					{
						url:require("../../../static/Network-Security/Hacker/HackerImageTwo.jpg"),
						CourTitle:"网络安全",
						CourTeacher:"华北水利水电大学 王畅 韩红玲 平源 李国佳 陈利军 孙全红 李秀芹 丁小娜 秦秀根",
						ViewPersonal:"1356"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Hacker-content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.HackerCont-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.HackerCont-scroll-item {
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
				
				.HackerCont_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
