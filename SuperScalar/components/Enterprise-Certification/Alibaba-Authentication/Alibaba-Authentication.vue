<template>
	<view class="Alibaba-Certification">
		<view class="Alibaba-Certification-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Alibaba-Certification_Collapse" style="padding: 0px 15px;">
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
				list:['ACA',"ACP","ACE"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Alibaba-Certification {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Alibaba-Certification-item {
			box-sizing: border-box;
			overflow: hidden;

			.Alibaba-Certification_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
