<template>
	<view class="TextualCriticism-Menu_content">
		<scroll-view scroll-x="true" show-scrollbar="false" class="TextualCriticism-Menu-scroll">
			<view class="TextualCriticism-Menu-scroll-box">
				<view class="TextualCriticism-Menu-box-item" :class="{active:menuindex == index}" @click="menuClick(item,index)" v-for="(item,index) in list" :key="index">
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
					"计算机等级证书",
					"计算机软件水平考试(软考)",
					"企业认证证书"
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
	.TextualCriticism-Menu_content{
		width: 100%;
		// height: 100%;
		display: flex;
		border-bottom: 2px solid #f5f5f5;
		border-radius: 5px;
		background-color: #b9c8ff;
		color: #111;
		box-sizing: border-box;
		
		.TextualCriticism-Menu-scroll {
			flex: 1;
			overflow: hidden;
			box-sizing: border-box;
		
			.TextualCriticism-Menu-scroll-box {
				display: flex;
				align-items: center;
				flex-wrap: nowrap;
				height: 45px;
				box-sizing: border-box;
		
				.TextualCriticism-Menu-box-item {
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