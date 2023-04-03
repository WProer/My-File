<template>
	<view class="list-content">
		<scroll-view scroll-x="true" show-scrollbar="false" class="navigatormenu-scroll">
			<view class="navigatormenu-scroll-box">
				<view class="navigatormenu-box-item" :class="{active:menuindex == index}" @click="menuClick(item,index)" v-for="(item,index) in list" :key="index">
					{{item}}
				</view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		name:"navigationMenu",
		props:{
			MenuIndex:{
				type:Number,
				default:0
			}
		},
		// 监听props和data值的变化
		watch:{
			MenuIndex(newValue,oldValue){
				// console.log(newValue,oldValue);
				this.menuindex = newValue
			}
		},
		data() {
			return {
				list:[
					"基础篇",
					"Web前端开发",
					"Web后端开发",
					"移动端开发",
					"游戏开发",
					"数字媒体",
					"人工智能",
					"网络安全"
				],
				menuindex:0
			};
		},
		
		methods:{
			menuClick(item,index){
				this.menuindex = index;
				this.$emit('navMenu',{
					data:item,
					index:index
				})
			}
		}
	}
</script>

<style lang="scss">
	.list-content{
		width: 100%;
		// height: 100%;
		display: flex;
		border-bottom: 2px solid #f5f5f5;
		border-radius: 5px;
		background-color: #b9c8ff;
		color: #111;
		box-sizing: border-box;
		
		.navigatormenu-scroll {
			flex: 1;
			overflow: hidden;
			box-sizing: border-box;
		
			.navigatormenu-scroll-box {
				display: flex;
				align-items: center;
				flex-wrap: nowrap;
				height: 45px;
				box-sizing: border-box;
		
				.navigatormenu-box-item {
					flex-shrink: 0;
					padding: 0px 15px;
					height: 100%;
					display: flex;
					align-items: center;
					
					&.active{
						color: #6678ff;
						// border: 1px solid #000;
						border-radius: 5px;
						box-shadow: 1px -1px 4px 1px #9c9999;
					}
				}
			}
		}
	}
</style>