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
				list:['网络工程师',"数据库工程师","信息安全工程师","嵌入式系统开发工程师","Linux应用与开发工程师"]
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
