<template>
	<view class="Cisco-Certification">
		<view class="Cisco-Certification-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Cisco-Certification_Collapse" style="padding: 0px 15px;">
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
				list:['CCNA',"CCNP","CCIE","CCIE LAB"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Cisco-Certification {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Cisco-Certification-item {
			box-sizing: border-box;
			overflow: hidden;

			.Cisco-Certification_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
