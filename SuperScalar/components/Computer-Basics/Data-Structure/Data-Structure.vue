<template>
	<view class="DataStructure-Content">
		<scroll-view class="DataStructure-scroll" scroll-x="true">
			<view class="DataStructure-scroll-item" v-for="(item,index) in CourData" :key="index">
				<image :src="item.url"></image>
				<!-- <image src="../../../static/Data-Structure/Data-StructureImg-one.jpg"></image> -->
				<text style="color: black;font-weight: 700;font-size: 18px;padding-left:2%;">{{item.CourTitle}}</text>
				<text style="color: #7a7a7a;padding-left:2%;margin-top: 7%;">{{item.CourTeacher}}</text>
				<view class="DataStructure_Views">
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
						url:require("../../../static/Data-Structure/Data-StructureImg-one.jpg"),
						CourTitle:"数据结构",
						CourTeacher:"浙江大学，陈越，何钦铭",
						ViewPersonal:"32255"
					},
					{
						url:require("../../../static/Data-Structure/Data-StructureImg-two.jpg"),
						CourTitle:"数据结构与算法",
						CourTeacher:"电子科技大学，林劼，戴波，刘震，周益民",
						ViewPersonal:"5323"
					},
					{
						url:require("../../../static/Data-Structure/Data-StructureImg-three.png"),
						CourTitle:"数据结构",
						CourTeacher:"厦门大学——郑旭玲，曾华琳，陈毅东，陈锦绣，庄朝晖",
						ViewPersonal:"671"
					},
					{
						url:require("../../../static/Data-Structure/Data-StructureImg-four.jpg"),
						CourTitle:"数据结构",
						CourTeacher:"苏州大学——孔芳，张玉华。唐自力，黄河",
						ViewPersonal:"212"
					}
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.DataStructure-Content {
		// height: 100%;
		// display: flex;
		// flex-direction: column;
		overflow: hidden;
		box-sizing: border-box;

		.DataStructure-scroll {
			height: 50%;
			white-space: nowrap;
			overflow: hidden;
			margin-top: 10px;

			.DataStructure-scroll-item {
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
				
				.DataStructure_Views{
					display: flex;
					justify-content: end;
				}
			}
		}


	}
</style>
