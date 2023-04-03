<template>
	<view class="Intermediate-Soft">
		<view class="Intermediate-Soft-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Intermediate-Soft_Collapse" style="padding: 0px 15px;">
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
				list:['软件测评师',"软件设计师","网络工程师","多媒体应用设计师","嵌入式系统设计师","电子商务设计师","系统集成项目管理工程师","信息系统监理师","数据库系统工程师","信息系统管理工程师","信息安全工程师","计算机辅助设计师","信息技术支持工程师","计算机硬件技术工程师","软件过程能力评估师"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Intermediate-Soft {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Intermediate-Soft-item {
			box-sizing: border-box;
			overflow: hidden;

			.Intermediate-Soft_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
