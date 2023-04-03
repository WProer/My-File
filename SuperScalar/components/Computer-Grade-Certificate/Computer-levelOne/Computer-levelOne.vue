<template>
	<view class="Computer-levelOne">
		<view class="Computer-levelOne-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Computer-levelOne_Collapse" style="padding: 0px 15px;">
								<Progress-Area></Progress-Area>
							</view>
						</uni-collapse-item>
					</uni-collapse>
				</view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:['WPS Office',"MS Office","Photoshop","网络安全素质教育"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Computer-levelOne {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Computer-levelOne-item {
			box-sizing: border-box;
			overflow: hidden;

			.Computer-levelOne_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
