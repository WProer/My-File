<template>
	<view class="content">
		<view class="image-view">
			<view class="head-portrait" @click="chooseImage()">
				
			</view>
			<view class="image-content">
				<p class="nickname">冰激凌</p>
				<p class="Sup-number">
					<span>晨旭号:123465789</span>
				</p>
			</view>
			
			<view class="image-link">
				<view class="link_arrow">
					<uni-icons type="forward" name="forward"></uni-icons>
				</view>
			</view>
		</view>
		
		<Per-center-button></Per-center-button>
		
		<Per-center-record></Per-center-record>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				src: "../../static/head-portrait13.jpg"
			}
		},
		onUnload() {

		},
		methods: {

			// 选择图片
			chooseImage() {
				const points = this;
				// 从本地相册选择图片或使用相机拍照
				uni.chooseImage({
					count: 1,
					success(res) {
						console.log("图片选择成功", res);
						const Path = res.tempFilePaths[0]
						const FileName = res.tempFiles[0].name
						console.log(Path);
						console.log(FileName);
						// 上传到云端
						uniCloud.uploadFile({
							// 要上传的文件对象
							filePath: Path, //要上传文件资源的路径 
							cloudPath: FileName, //阿里云文件名
							success(res) {
								console.log("上传成功文件：", res);
								points.src = res.fileID
							}
						})
					},
					fail(err) {
						console.log(err);
					}

				})


			}

		},
	}
</script>


<style lang="scss">
	$Color:#A6E4FC;
	$bor_Color:#2b2c2d;
	$text-Color-one:#3289e7;
	
	page{
		margin: 0px;
		padding: 0px;
		// height: 100%;
		display: flex;
		overflow: hidden;
		box-sizing: border-box;
		
		// .uni-app--showtabbar{
		// 	background-color: $base-color;
		// }
	}
	
	.content{
		background-color: $base-color;
		overflow: hidden;
		box-sizing: border-box;
		width: 100%;
		height: 97%;
		display: flex;
		flex-direction: column;
	}

	.image-view {
		width: 97%;
		height: 125px;
		border: 1px solid $Color;
		border-radius: 10px;
		margin-top: 20px;
		margin-left: 5px;
		display: flex;
		justify-content: space-around;
		align-items: center;

		.head-portrait {
			height: 100px;
			width: 100px;
			border: 1px solid $bor_Color;
			border-radius: 10px;
			background-image: url('../../static/head-portrait13.jpg');
			background-size: cover;

		}
		
		.image-content{
			width: 140px;
			height: 100%;
			display: flex;
			flex-direction: column;
			justify-content: space-around;
			
			.nickname{
				flex: 1;
				color: #fff;
				font-size: 25px;
				font-weight: 700;
				margin-top: 13px;
			}
			
			.Sup-number{
				flex: 2;
				color: #fff;
				font-size: 15px;
				font-weight: 700;
				display: inline-block;
				margin-top: 45px;
			}
			
		}
		
		.image-link{
			width: 50px;
			height: 100%;
			
			.link_arrow{
				width: 100%;
				height: 100%;
				display: flex;
				justify-content: center;
				align-items: center;
				
				::v-deep .uni-icons{
					font-size: 35px !important; 
					color: #fff !important;
				}
			}
		}
	}
</style>
