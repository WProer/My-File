<template>
	<view class="Reminder-Settings">
		<checkbox-group @change="checkboxChange">
			<label class="Reminder-Settings_label" v-for="item in items" :key="item.value">
				<view>
					<checkbox :value="item.value" :checked="item.checked" />
				</view>
				<view>{{item.name}}</view>
			</label>
		</checkbox-group>
		<view class="Reminder-Settings_Button">
			<button @click="Saved()">保存</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				items: [{
						value: '基础篇',
						name: '基础篇',
						checked: 'true'
					},
					{
						value: 'Web前端开发',
						name: 'Web前端开发',
						checked: 'true'
					},
					{
						value: 'Web后端开发',
						name: 'Web后端开发'
					},
					{
						value: '移动端开发',
						name: '移动端开发'
					},
					{
						value: '游戏开发',
						name: '游戏开发'
					},
					{
						value: '数字媒体',
						name: '数字媒体'
					},
					{
						value: '人工智能',
						name: '人工智能'
					},
					{
						value: '网络安全',
						name: '网络安全'
					}

				]
			}
		},
		methods: {
			checkboxChange: function(e) {
				var items = this.items,
					values = e.detail.value;
				for (var i = 0, lenI = items.length; i < lenI; ++i) {
					const item = items[i]
					if (values.includes(item.value)) {
						this.$set(item, 'checked', true)
					} else {
						this.$set(item, 'checked', false)
					};
					
				};
			},
			
			Saved(){
				uni.showToast({
					icon:'success',
					title:"保存成功！",
					duration:2000
				})
			}
		}
	}
</script>

<style lang="scss">
.Reminder-Settings{
	padding: 30px;
	
	.Reminder-Settings_label{
		display: flex;
		justify-content: flex-start;
		border: 1px solid #ccc;
		border-radius: 5px;
		margin: 10px 0px;
		padding: 10px;
		background-color: #fcfcfc;
	}
	
	.Reminder-Settings_Button{
		padding: 20px 100px;
		
		button{
			background-color: $base-color;
		}
	}
}
</style>
