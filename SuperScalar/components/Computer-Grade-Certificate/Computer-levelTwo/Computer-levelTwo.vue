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
				list:['C语言程序设计',"Java语言程序设计","Access数据库程序设计","C++语言程序设计","MySQL数据库程序设计","Web程序设计","MS Office高级应用与设计","Python语言程序设计","wPS Office高级应用与设计","openGauss数据库程序设计"]
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
