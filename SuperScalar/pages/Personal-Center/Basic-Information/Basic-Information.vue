<template>
	<view class="Basic-Information">
		<form class="Basic-Information_form" action="">
			<view class="NAME form-item_input">
				<text>真实姓名:</text><input type="text" name="" id="" required>
			</view>
			<view class="SEX form-item_input">
				<text>性别:</text>
				<radio-group name="">
					<label>
						<radio value="保密" /><text>保密</text>
					</label>
					<label style="margin-left: 10px;">
						<radio value="男" /><text>男</text>
					</label>
					<label style="margin-left: 10px;">
						<radio value="女" /><text>女</text>
					</label>
				</radio-group>
			</view>
			<view class="EMAIL form-item_input">
				<text>电子邮箱:</text><input type="email" name="" id="">
			</view>
			<view class="PHONE form-item_input">
				<text>电话号码:</text><input type="number" name="" id="" required>
			</view>
			<view class="QQ form-item_input">
				<text>QQ:</text><input type="number" name="" id="" required>
			</view>
			<view class="ADDRESS form-item_input">
				<text>所在地址:</text>
				<select name="" id="">
					<option value="">省级地区</option>
					<option v-for="(item,index) in province" :value="index">{{item.ProvinceName}}</option>
				</select>
				<select name="" id="" style="margin-left: 10px;">
					<option value="">市级地区</option>
				</select>
				<select name="" id="" style="margin-left: 10px;">
					<option value="">县/区</option>
				</select>
			</view>
			<view class="POSTAL——ADD form-item_input">
				<text>通讯地址:</text><input type="text" name="" id="" required>
			</view>
			<view class="POSTAL——CODE form-item_input">
				<text>邮编:</text><input type="text" name="" id="" required>
			</view>
			<view class="BIRTHDAY form-item_input">
				<text>出生年月:</text>
				<picker mode="date" :value="date" :start="startDate" :end="endDate" @change="bindDateChange" required>
					<view>{{ date }}</view>
				</picker>
			</view>
			<view class="TRADE form-item_input">
				<text>从事行业:</text>
				<select name="" id="" required>
					<option value="">请选择你所从事的行业</option>
					<option v-for="(item,index) in trade" :value="index">{{item.name}}</option>
				</select>
			</view>
			<view class="BUTTON form-item_input">
				<button form-type="submit">提交</button>
				<button form-type="reset">重置</button>
			</view>


		</form>
	</view>
</template>

<script>
	import graceChecker from '../../../common/graceChecker.js'
	function getDate(type) {
		const date = new Date();

		let year = date.getFullYear();
		let month = date.getMonth() + 1;
		let day = date.getDate();

		if (type === 'start') {
			year = year - 100;
		} else if (type === 'end') {
			year = year + 1;
		}
		month = month > 9 ? month : '0' + month;
		day = day > 9 ? day : '0' + day;

		return `${year}-${month}-${day}`;
	}
	export default {
		data() {
			return {
				province: [{
						ProvinceName: "北京市"
					},
					{
						ProvinceName: "天津市"
					},
					{
						ProvinceName: "上海市"
					},
					{
						ProvinceName: "重庆市"
					},
					{
						ProvinceName: "河北省"
					},
					{
						ProvinceName: "山西省"
					},
					{
						ProvinceName: "辽宁省"
					},
					{
						ProvinceName: "吉林省"
					},
					{
						ProvinceName: "黑龙江省"
					},
					{
						ProvinceName: "江苏省"
					},
					{
						ProvinceName: "浙江省"
					},
					{
						ProvinceName: "安徽省"
					},
					{
						ProvinceName: "福建省"
					},
					{
						ProvinceName: "江西省"
					},
					{
						ProvinceName: "山东省"
					},
					{
						ProvinceName: "河南省"
					},
					{
						ProvinceName: "湖北省"
					},
					{
						ProvinceName: "湖南省"
					},
					{
						ProvinceName: "广东省"
					},
					{
						ProvinceName: "海南省"
					},
					{
						ProvinceName: "四川省"
					},
					{
						ProvinceName: "贵州省"
					},
					{
						ProvinceName: "云南省"
					},
					{
						ProvinceName: "陕西省"
					},
					{
						ProvinceName: "甘肃省"
					},
					{
						ProvinceName: "青海省"
					},
					{
						ProvinceName: "台湾省"
					},
					{
						ProvinceName: "内蒙古自治区"
					},
					{
						ProvinceName: "广西壮族自治区"
					},
					{
						ProvinceName: "西藏自治区"
					},
					{
						ProvinceName: "宁夏回族自治区"
					},
					{
						ProvinceName: "新疆维吾尔自治区"
					},
					{
						ProvinceName: "香港特别行政区"
					},
					{
						ProvinceName: "澳门特别行政区"
					}
				],
				date: getDate({
					format: true
				}),
				startDate: getDate('start'),
				endDate: getDate('end'),
				trade: [{
						name: "在校学生"
					},
					{
						name: "计算机·网络·技术"
					},
					{
						name: "经营管理"
					},
					{
						name: "娱乐业"
					},
					{
						name: "文体工作"
					},
					{
						name: "销售"
					},
					{
						name: "医疗卫生"
					},
					{
						name: "农林牧鱼劳动者"
					},
					{
						name: "酒店·餐饮·旅游·其他服务"
					},
					{
						name: "美术·设计·创意"
					},
					{
						name: "外出务工人员"
					},
					{
						name: "贸易·物流·采购·运输"
					},
					{
						name: "建筑·房地产·装饰装修·物业管理"
					},
					{
						name: "财务·审计·统计"
					},
					{
						name: "电力·能源·动力"
					},
					{
						name: "个体经营·商业零售"
					},
					{
						name: "军人警察"
					},
					{
						name: "美容保健"
					},
					{
						name: "行政·后勤"
					},
					{
						name: "教育·培训"
					},
					{
						name: "党政机关事业工作者·公务员类"
					},
					{
						name: "市场·公关·咨询·媒介"
					},
					{
						name: "技工"
					},
					{
						name: "工厂生产"
					},
					{
						name: "宗教、神职人员"
					},
					{
						name: "工程师"
					},
					{
						name: "新闻出版·文化工作"
					},
					{
						name: "金融"
					},
					{
						name: "人力资源"
					},
					{
						name: "保险"
					},
					{
						name: "法律"
					},
					{
						name: "翻译"
					},
					{
						name: "自由职业者"
					},
					{
						name: "待业/无业/失业"
					},
					{
						name: "其他"
					}
				],
			}
		},
		methods: {
			bindDateChange: function(e) {
				this.date = e.detail.value;
			},
			formSubmit: function(e) {
				console.log('form发生了submit事件，携带数据为：' + JSON.stringify(e.detail.value))
			    //定义表单规则
			    var rule = [
			        {name:"nickname", checkType : "string", checkRule:"1,3",  errorMsg:"姓名应为1-3个字符"},
			        {name:"gender", checkType : "in", checkRule:"男,女",  errorMsg:"请选择性别"},
			        {name:"loves", checkType : "notnull", checkRule:"",  errorMsg:"请选择爱好"}
			    ];
			    //进行表单检查
			    var formData = e.detail.value;
			    var checkRes = graceChecker.check(formData, rule);
			    if(checkRes){
			        uni.showToast({title:"验证通过!", icon:"none"});
			    }else{
			        uni.showToast({ title: graceChecker.error, icon: "none" });
			    }
			},
			formReset: function(e) {
				console.log('清空数据')
			}
		}
	}
</script>

<style lang="scss">
	.Basic-Information {
		width: 100%;
		height: 800px;
		overflow: hidden;
		box-sizing: border-box;
		font-weight: 700;

		.form-item_input {
			overflow: hidden;
			box-sizing: border-box;
			display: flex;
			border-bottom: 1px solid #ccc;
			padding: 20px 30px;

			text {
				flex-shrink: 1;
				width: 30%;
				overflow: hidden;
				box-sizing: border-box;
			}

			input {

				border: 1px solid black;
			}

			button {
				width: 80px;
				background-color: $base-color;
				color: #fff;
			}
		}

		.BUTTON {
			border: none;
			
		}


	}
</style>
