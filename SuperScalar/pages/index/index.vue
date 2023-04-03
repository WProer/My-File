<template>
	<view class="content">
		<view class="index-search">
			<index-search></index-search>
		</view>
		<view class="index-Rotation">
			<index-Rotation></index-Rotation>
		</view>
		<view class="navigationMenu">
			<navigationMenu @navMenu="navMenu" :MenuIndex='MenuIndex'></navigationMenu>
		</view>
		<view class="substance">
			<learning-swiper @change='change' :listSwiperIndex='listSwiperIndex'></learning-swiper>
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
		onLoad() {

		},
		methods: {
			navMenu({
				data,
				index
			}) {
				// console.log(data, index);
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

	.content {
		width: 100%;
		display: flex;
		flex-direction: column;
		flex: 1;
		background-color: $base-color;

		.index-search {
			width: 100%;
			height: 23%;
			box-sizing: border-box;
		}

		.index-Rotation {
			width: 100%;
			height: 45%;
			overflow: hidden;
			box-sizing: border-box;
		}

		.navigationMenu {
			width: 100%;
			height: 13%;
			overflow: hidden;
			box-sizing: border-box;
		}

		.substance {
			width: 100%;
			height: 100%;
			overflow: hidden;
			box-sizing: border-box;
		}
	}
</style>
