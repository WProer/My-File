<template>
	<view class="Network-Security">
		<scroll-view class="scroll-list" scroll-y="true">
			<view class="Network-Security_item">
				<text>密码学 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<Cryptography></Cryptography>
				</view>
			</view>
			<view class="Network-Security_item">
				<text>黑客攻防 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<Hacker></Hacker>
				</view>
			</view>
			<view class="Network-Security_item">
				<text>逆向工程 <text>_______</text> <text>推荐课程</text></text>
				<view class="C-Language_item">
					<ReverseEngineering></ReverseEngineering>
				</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import Cryptography from "./cryptography/cryptography.vue"
	import Hacker from "./Hacker/Hacker.vue"
	import ReverseEngineering from "./reverse-engineering/reverse-engineering.vue"
	export default {
		name: "Learning",
		data() {
			return {

			};
		},
		components: {
			Cryptography,
			Hacker,
			ReverseEngineering
		}
	}
</script>

<style lang="scss">
	.Network-Security {
		height: 100%;
		display: flex;
		flex-direction: column;
		flex: 1;
		overflow: hidden;
		box-sizing: border-box;
		padding: 0px 5px;

		.scroll-list {
			height: 100%;
			display: flex;
			flex: 1;
			flex-direction: column;

			.Network-Security_item {
				height: 60%;
				border: 1px solid #00ffff;
				background-color: #fff;
				overflow: hidden;
				box-sizing: border-box;
				padding: 5px 10px;
				border-radius: 10px;
				margin-bottom: 10px;

				text {
					width: 100%;
					font-size: 25px;
					color: #aaaaff;
					font-weight: 700;

					text {
						font-size: 15px;
					}
				}

				.C-Language_item {
					height: 100%;
					width: 100%;
					overflow: hidden;
					box-sizing: border-box;
				}
			}
		}
	}
</style>
