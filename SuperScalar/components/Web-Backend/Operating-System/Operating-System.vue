<template>
	<view class="OperatingSystem-Content">
		<scroll-view class="OperatingSystem-scroll" scroll-x="true">
			<view class="OperatingSystem-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/WebBackend/OperatingSystem/OperatingSystem-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="OperatingSystem_Views">
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
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-one.jpg"),
						CourTitle:"计算机网络",
						CourTeacher:"哈尔滨工业大学——李全龙、聂兰顺",
						ViewPersonal:"23146"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-two.jpg"),
						CourTitle:"计算机网络",
						CourTeacher:"东北大学——姚羽",
						ViewPersonal:"46548"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-three.jpg"),
						CourTitle:"计算机网络基础及应用",
						CourTeacher:"南京理工大学——丁晟春",
						ViewPersonal:"56835"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-four.jpg"),
						CourTitle:"计算机操作系统",
						CourTeacher:"南京大学——骆斌、葛季栋",
						ViewPersonal:"23486"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-five.png"),
						CourTitle:"玩转计算机网络-计算机网络原理",
						CourTeacher:"青岛大学——云红艳、胡志球、高磊",
						ViewPersonal:"2335"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-six.jpg"),
						CourTitle:"计算机网络",
						CourTeacher:"安阳师范学院——陈卫军、平静、刘海、黄永灿、赵元庆",
						ViewPersonal:"13489"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-seven.png"),
						CourTitle:"计算机网络系统",
						CourTeacher:"电子科技大学——傅翀、郭文生、刘梦娟、王瑞锦、张翔、兰刚、王伟东、黄俊",
						ViewPersonal:"1461"
					},
					{
						url:require("../../../static/WebBackend/OperatingSystem/OperatingSystem-eight.jpg"),
						CourTitle:"计算机网络",
						CourTeacher:"郑州西亚斯学院——谢泽奇、师晓利、宋小芹、王芳、丁小娜",
						ViewPersonal:"73049"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.OperatingSystem-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.OperatingSystem-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.OperatingSystem-scroll-item {
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
				
				.OperatingSystem_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
