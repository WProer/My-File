<template>
	<view class="BackTop" @click="BackTop()">
		<uni-icons type="top"></uni-icons>
	</view>
</template>

<script>
	export default {
		name: "BackTop",
		data() {
			return {

			};
		},
		methods:{
			BackTop(){
				uni.pageScrollTo({
					scrollTop:0,
					duration:1000
				})
			}
		}
	}
</script>

<style lang="scss">
	.BackTop {
		width: 50px;
		height: 50px;
		background-color: #b9c8ff;
		border-radius: 25px;
		position: fixed;
		margin-left: 83%;
		margin-top: 170%;
		opacity: 0.7;
		display: flex;
		justify-content: center;
		align-items: center;
		
		.uni-icons{
			font-size: 30px !important;
			font-weight: 700 !important;
			color: #fff !important;
		}
	}
</style>
