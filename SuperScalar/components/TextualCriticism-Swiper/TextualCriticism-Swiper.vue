<template>
	<view class="TextualCriticism-Swiper-content">
		<swiper class="home" :current="listSwiperIndex" @change="change">
			<swiper-item>
				<view class="swiper-item">
					<Computer-Grade-Certificate></Computer-Grade-Certificate>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Computer-Software-Test></Computer-Software-Test>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<Enterprise-Certification></Enterprise-Certification>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		name: "TextualCriticism-Swiper",
		props: {
			listSwiperIndex: {
				type: Number,
				default: 0
			}
		},
		data() {
			return {

			};
		},
		methods: {
			change(e) {
				// console.log(e);
				const {
					current
				} = e.detail;
				this.$emit('change', current)
			}
		}
	}
</script>

<style lang="scss">
	.TextualCriticism-Swiper-content {
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
