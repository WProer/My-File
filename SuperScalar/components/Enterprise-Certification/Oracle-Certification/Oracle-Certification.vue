<template>
	<view class="Oracle-Certification">
		<view class="Oracle-Certification-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Oracle-Certification_Collapse" style="padding: 0px 15px;">
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
				list:['OCA认证专员',"OCP认证专家","OCM认证大师"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Oracle-Certification {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Oracle-Certification-item {
			box-sizing: border-box;
			overflow: hidden;

			.Oracle-Certification_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
