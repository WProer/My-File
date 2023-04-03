<template>
	<view class="Microsorft-Certification">
		<view class="Microsorft-Certification-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Microsorft-Certification_Collapse" style="padding: 0px 15px;">
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
				list:['安全工程师',"安全运营分析员","标识和访问管理员","风险实践者","管理员","技术主管","解决方案架构师","开发人员","网络工程师"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Microsorft-Certification {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Microsorft-Certification-item {
			box-sizing: border-box;
			overflow: hidden;

			.Microsorft-Certification_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
