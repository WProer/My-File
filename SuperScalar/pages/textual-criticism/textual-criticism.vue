<template>
	<view class="content">
		<view class="Topic-Exercise-Area">
			<Topic-Exercise></Topic-Exercise>
		</view>
		<view class="Question-Making-Area">
			<Question-Making></Question-Making>
		</view>
		<view class="TextualCriticism-Menu">
			<TextualCriticism @navMenu="navMenu" :MenuIndex='MenuIndex'></TextualCriticism>
		</view>
		<view class="TextualCriticism-Swiper">
			<TextualCriticism-Swiper  @change='change' :listSwiperIndex='listSwiperIndex'></TextualCriticism-Swiper>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				MenuIndex: 0,
				listSwiperIndex: 0
			}
		},
		methods: {
			navMenu({
				data,
				index
			}) {
				console.log(data, index);
				this.listSwiperIndex = index
			},
			change(current){
				// console.log(current);
				this.MenuIndex = current
			}
		}
	}
</script>

<style lang="scss">
page {
		height: 100%;
		display: flex;
	}
	
	.content{
		width: 100%;
		display: flex;
		flex-direction: column;
		flex: 1;
		background-color: $base-color;
		
		.Topic-Exercise-Area{
			width: 100%;
		}
		
		.Question-Making-Area{
			width: 100%;
		}
		
		.TextualCriticism-Menu {
			width: 100%;
			height: 13%;
			overflow: hidden;
			box-sizing: border-box;
			margin-top: 10px;
		}
		
		.TextualCriticism-Swiper{
			width: 100%;
			height: 100%;
			overflow: hidden;
			box-sizing: border-box;
		}
	}
</style>
