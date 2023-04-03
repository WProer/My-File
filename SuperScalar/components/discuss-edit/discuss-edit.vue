<template>
	<view class="discuss-edit" @click="DiscussADD()">
		<uni-icons type="compose"></uni-icons>
	</view>
</template>

<script>
	export default {
		name:"discuss-edit",
		data() {
			return {
				
			};
		},
		methods:{
			DiscussADD(){
				console.log(123);
				uni.navigateTo({
					url:"/pages/DiscussAdd/DiscussAdd"
				})
			}
		}
	}
</script>

<style lang="scss">
	.discuss-edit {
		width: 50px;
		height: 50px;
		background-color: #b9c8ff;
		border-radius: 25px;
		position: fixed;
		margin-left: 83%;
		margin-top: 155%;
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