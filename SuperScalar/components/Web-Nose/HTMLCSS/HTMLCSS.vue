<template>
	<view class="HTMLCSS-Content">
		<scroll-view class="HTMLCSS-scroll" scroll-x="true">
			<view class="HTMLCSS-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Web-Nose/HTMLCSS/HTMLIMG-one.png"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="HTMLCSS_Views">
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
						url:require("../../../static/Web-Nose/HTMLCSS/HTMLIMG-one.png"),
						CourTitle:"网页制作基础及HTML",
						CourTeacher:"江苏开发大学，刘芳，许小媛，刘田田",
						ViewPersonal:"865"
					},
					{
						url:require("../../../static/Web-Nose/HTMLCSS/HTMLIMG-two.png"),
						CourTitle:"网页制作（HTML5+CSS3）",
						CourTeacher:"宁波城市职业技术学院，郑哲",
						ViewPersonal:"184"
					},
					{
						url:require("../../../static/Web-Nose/HTMLCSS/HTMLIMG-three.png"),
						CourTitle:"H5移动应用开发",
						CourTeacher:"河北软件职业技术学院——来继敏，郭春雷，张莹，丁宏伟，贺晨，崔秀艳，刘红艳，薛玉倩",
						ViewPersonal:"31"
					},
					{
						url:require("../../../static/Web-Nose/HTMLCSS/HTMLIMG-four.png"),
						CourTitle:"HTMl5网页前端设计",
						CourTeacher:"青岛职业技术学院——苗彩霞，常中华，高桂霞，刘志敏",
						ViewPersonal:"580"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.HTMLCSS-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.HTMLCSS-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.HTMLCSS-scroll-item {
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
				
				.HTMLCSS_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
