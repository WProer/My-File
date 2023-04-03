<template>
	<view class="Advanced-Soft">
		<view class="Advanced-Soft-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Advanced-Soft_Collapse" style="padding: 0px 15px;">
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
				list:['信息系统项目管理师',"系统分析师","系统架构设计师","网络规划设计师","系统规划与管理师"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Advanced-Soft {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Advanced-Soft-item {
			box-sizing: border-box;
			overflow: hidden;

			.Advanced-Soft_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
