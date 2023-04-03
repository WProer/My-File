<template>
	<view class="learning-swiper">
		<swiper class="home" :current="listSwiperIndex" @change="change">
			<swiper-item>
				<view class="swiper-item">
					<Computer-Basics></Computer-Basics>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Web-Nose></Web-Nose>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Web-Backend></Web-Backend>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Mobile-Development></Mobile-Development>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Game-Development></Game-Development>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Digital-Media></Digital-Media>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Artificial-Intelligence></Artificial-Intelligence>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Network-Security></Network-Security>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		name:"learning-swiper",
		props:{
			listSwiperIndex:{
				type:Number,
				default:0
			}
		},
		data() {
			return {
				
			};
		},
		methods:{
			change(e){
				// console.log(e);
				const {current} = e.detail;
				this.$emit('change',current)
			}
		}
	}
</script>

<style lang="scss">
	.learning-swiper {
		height: 100%;
		overflow: hidden;

		.home {
			height: 100%;
			overflow: hidden;

			.swiper-item {
				height: 100%;
				overflow: hidden;
			}
		}
	}
</style>