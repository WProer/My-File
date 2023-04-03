<template>
	<view class="Adobe-Certification">
		<view class="Adobe-Certification-item">
			<scroll-view scroll-y="true">
				<view>
					<uni-collapse>
						<uni-collapse-item v-for="(item,index) in list" :key="index" :title="item">
							<view class="Adobe-Certification_Collapse" style="padding: 0px 15px;">
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
				list:['Photoshop',"Illustrator","InDesign","Flash","Dreamweaver","Fireworks","AfterEffects","Premiere","Acrobat"]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.Adobe-Certification {
		margin-top: 10px;
		overflow: hidden;
		box-sizing: border-box;

		.Adobe-Certification-item {
			box-sizing: border-box;
			overflow: hidden;

			.Adobe-Certification_Collapse {
				height: 65px;
				overflow: hidden;
				box-sizing: border-box;
			}
		}
	}
</style>
