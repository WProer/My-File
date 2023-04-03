<template>
	<view class="DataBank-Content">
		<scroll-view class="DataBank-scroll" scroll-x="true">
			<view class="DataBank-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Data-Bank/Data-BankImg-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="DataBank_Views">
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
						url:require("../../../static/Data-Bank/Data-BankImg-one.jpg"),
						CourTitle:"数据库技术及应用",
						CourTeacher:"东北师范大学，李雁翎，罗娜，曾毅，王红岩，张靖波，浦东兵",
						ViewPersonal:"1156"
					},
					{
						url:require("../../../static/Data-Bank/Data-BankImg-two.jpg"),
						CourTitle:"数据库系统原理",
						CourTeacher:"北京师范大学，党德鹏",
						ViewPersonal:"3479"
					},
					{
						url:require("../../../static/Data-Bank/Data-BankImg-three.jpg"),
						CourTitle:"SQL数据库设计",
						CourTeacher:"咸阳职业技术学院——王雪侠，许珂乐，张莹，张耸",
						ViewPersonal:"789"
					},
					{
						url:require("../../../static/Data-Bank/Data-BankImg-four.jpg"),
						CourTitle:"SQL Server 2016数据库及应用",
						CourTeacher:"陕西国防工业职业技术学院——马静，戚斌，李小遐，郭立文，严博文，常玲玲",
						ViewPersonal:"1102"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.DataBank-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.DataBank-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.DataBank-scroll-item {
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
				
				.DataBank_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
