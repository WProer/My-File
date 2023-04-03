<template>
	<view class="Enterprise-Certification-Certificate">
		
		<scroll-view class="scroll-list" scroll-y="true" >
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>微软认证考试 <text>_______</text> <text>知识点练习</text></text>
						<MicrosoftCertification></MicrosoftCertification>
					</view>
				</scroll-view>
			</view>
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>Adobe认证考试 <text>_______</text> <text>知识点练习</text></text>
						<AdobeCertification></AdobeCertification>
					</view>
				</scroll-view>
			</view>
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>Oracle认证<text>_______</text> <text>知识点练习</text></text>
						<OracleCertification></OracleCertification>
					</view>
				</scroll-view>
			</view>
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>JAVA认证<text>_______</text> <text>知识点练习</text></text>
						<JAVACertification></JAVACertification>
					</view>
				</scroll-view>
			</view>
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>Cisco认证<text>_______</text> <text>知识点练习</text></text>
						<CiscoCertification></CiscoCertification>
					</view>
				</scroll-view>
			</view>
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>阿里云（ACA、ACP、ACE）认证<text>_______</text> <text>知识点练习</text></text>
						<AlibabaCertification></AlibabaCertification>
					</view>
				</scroll-view>
			</view>
			<view class="Enterprise-Certification_item">
				<scroll-view class="scroll-list" scroll-y="true" >
					<view class="Enterprise-Certification_item" style="border: none; height: auto;">
						<text>CDA数据分析师认证<text>_______</text> <text>知识点练习</text></text>
						<CDACertification></CDACertification>
					</view>
				</scroll-view>
			</view>
		</scroll-view>
		
		
	</view>
</template>

<script>
	import MicrosoftCertification from "./Microsoft-Certification/Microsoft-Certification.vue"
	import AdobeCertification from "./Adobe-Certification/Adobe-Certification.vue"
	import OracleCertification from "./Oracle-Certification/Oracle-Certification.vue"
	import JAVACertification from "./JAVA-Certification/JAVA-Certification.vue"
	import CiscoCertification from "./Cisco-Certification/Cisco-Certification.vue"
	import AlibabaCertification from "./Alibaba-Authentication/Alibaba-Authentication.vue"
	import CDACertification from "./CDA-Certification/CDA-Certification.vue"
	export default {
		name:"Enterprise-Certification-Certificate",
		data() {
			return {
				
			};
		},
		components:{
			MicrosoftCertification,
			AdobeCertification,
			OracleCertification,
			JAVACertification,
			CiscoCertification,
			AlibabaCertification,
			CDACertification
		}
	}
</script>

<style lang="scss">
	.Enterprise-Certification-Certificate{
		height: 100%;
		display: flex;
		flex-direction: column;
		flex: 1;
		overflow: hidden;
		box-sizing: border-box;
		padding: 0px 5px;
		
		.scroll-list{
			height: 100%;
			margin-top: 10px;
			display: flex;
			flex: 1;
			flex-direction: column;
			overflow: hidden;
			box-sizing: border-box;
			
			.Enterprise-Certification_item{
				height: 300px;
				background-color: #f1f1ff;
				border: 1px solid #00ffff;
				border-radius: 10px;
				overflow: hidden;
				box-sizing: border-box;
				padding: 5px 10px;
				margin-bottom: 10px;
				
				text{
					width: 100%;
					font-size: 15px;
					color: #aaaaff;
					font-weight: 700;
					
					text{
						font-size: 10px;
					}
				}
			}
		}
	}

</style>