<template>
	<view class="CDA-Certification">
		<view class="CDA-Certification-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="CDA-Certification_Collapse" style="padding: 0px 15px;">
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
				list:['CDALevelⅠ',"CDALevelⅡ","CDALevelⅢ"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.CDA-Certification {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.CDA-Certification-item {
			box-sizing: border-box;
			overflow: hidden;

			.CDA-Certification_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
