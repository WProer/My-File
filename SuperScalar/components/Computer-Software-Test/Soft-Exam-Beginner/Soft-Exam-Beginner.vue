<template>
	<view class="Soft-Ceginner">
		<view class="Soft-Ceginner-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Soft-Ceginner_Collapse" style="padding: 0px 15px;">
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
				list:['程序员',"网络管理员","信息处理技术员","信息系统运行管理员","网页制作员","电子商务技术员","多媒体应用制作技术员"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Soft-Ceginner {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Soft-Ceginner-item {
			box-sizing: border-box;
			overflow: hidden;

			.Soft-Ceginner_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
