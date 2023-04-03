<template>
	<view class="Rotation-content">
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" indicator-color="#fff"
			indicator-active-color="#99CCFF" circular="true`">
			<swiper-item>
				<view class="swiper-item">
					<image src="../../static/Carousel1.png" mode=""></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="../../static/Carousel2.png" mode=""></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="../../static/Carousel3.png" mode=""></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="../../static/Carousel4.png" mode=""></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		name: "index-Rotation",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.Rotation-content {
		width: 100%;
		// height: 60%;
		padding: 10px 10px;
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.swiper-item {
			width: 100%;
			height: 100%;
			overflow: hidden;
			box-sizing: border-box;
			padding: 0px 10px;

			image {
				width: 100%;
				height: 100%;
				overflow: hidden;
				box-sizing: border-box;
				border-radius: 10px;
			}

		}
	}
</style>
