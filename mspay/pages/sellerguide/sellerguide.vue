<template>
	<view>
		<cu-custom class="title" bgColor="bg-yellow" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">悦知付</block>
		</cu-custom>
		<view class="margin-top-xl  padding-xs bg-yellow flex align-center">
			
			<view class="flex-sub text-center">
				<view class=" text-xl padding">
					<text class="text-black text-bold">内容付费 知识变现</text>
				</view>
				
			</view>
		</view>
		<view class="bg-yellow solids-bottom padding-xs flex align-center">
			
			<view class="flex-sub text-center">
				<view class="solid-bottom text-lg padding">
					<text class="text-black">Make your content more valuable</text>
				</view>
				<view class="padding">内容付费，让知识更具价值</view>
			</view>
		</view>
		<view class="padding bg-white">
			<view class="flex">
				<view class="flex-sub bg-gradual-blue padding-sm margin-xs radius">
					<view class=" padding-xs flex align-center">
						<view class="flex-sub text-center">
							<view class="solid-bottom text-xsl ">
								<text class=" cuIcon-roundcheckfill text-green"></text>
							</view>
							<view class=" text-sm ">知识付费</view>
							<view class=" text-xs padding-top-xl">商家将视频、素材、文档或是软件等等信息进行隐藏，用户付费之后可以显示该隐藏内容</view>
						</view>
					</view>
				</view>
				<view class="flex-sub bg-gradual-orange padding-sm margin-xs radius">
					<view class=" padding-xs flex align-center">
						<view class="flex-sub text-center">
							<view class="solid-bottom text-xsl ">
								<text class=" cuIcon-roundcheckfill text-green"></text>
							</view>
							<view class=" text-sm ">资源付费</view>
							<view class=" text-xs padding-top-xl">商家将视频、素材、文档或是软件等等信息进行隐藏，用户付费之后可以显示该隐藏内容</view>
						</view>
					</view>
							
				</view>
				<view class="flex-sub bg-gradual-purple padding-sm margin-xs radius">
						<view class=" padding-xs flex align-center">
						<view class="flex-sub text-center">
							<view class="solid-bottom text-xsl ">
								<text class=" cuIcon-roundcheckfill text-green"></text>
							</view>
							<view class=" text-sm ">账号付费</view>
							<view class=" text-xs padding-top-xl">论坛账号、激活码，商家设定多个卡密内容，用户购买后自动发货，每个人可得到不同的内容</view>
						</view>
					</view>
				</view>
			</view>
			</view>
	<view class="padding-xs flex align-center bg-white">
			
				<view class="flex-sub text-center">
					<view class=" text-lg padding">
						<text class="text-black">方案概述</text>
					</view>
				
				</view>
			</view>
			
			<view class="padding bg-white">
				
				<view class="text-center padding">发个卡是数贝网络科技提供的内容付费平台。
				同时面向商家与消费者。其主要功能为内容付费后可见，
				即商家在平台发布要隐藏的内容，商家可将该商品嵌入到自己博客、
				论坛或是任意网页中，用户只有在付费后才可见内容。
				</view>
			</view>
			
			<view class="flex bg-white">
				<view class="flex-sub bg-white padding-sm margin-xs radius">
					<view class=" padding-xs flex align-center">
						<view class="flex-sub text-center">
							<view class="solid-bottom text-xsl ">
								<text class=" cuIcon-roundcheckfill text-green"></text>
							</view>
							<view class=" text-sm ">十元结算</view>
							<view class=" text-xs padding-top-xl">超低结算条件，只要您通过平台实现可结算金额超过10元。就达到了结算条件。</view>
						</view>
					</view>
				</view>
				<view class="flex-sub bg-white padding-sm margin-xs radius">
					<view class=" padding-xs flex align-center">
						<view class="flex-sub text-center">
							<view class="solid-bottom text-xsl ">
								<text class=" cuIcon-roundcheckfill text-green"></text>
							</view>
							<view class=" text-sm ">超低费率</view>
							<view class=" text-xs padding-top-xl">每笔交易最低收取5%的费用。比如成交10元订单，平台仅仅收取5毛钱。</view>
						</view>
					</view>
							
				</view>
				<view class="flex-sub bg-white padding-sm margin-xs radius">
						<view class=" padding-xs flex align-center">
						<view class="flex-sub text-center">
							<view class="solid-bottom text-xsl ">
								<text class=" cuIcon-roundcheckfill text-green"></text>
							</view>
							<view class=" text-sm ">结算及时</view>
							<view class=" text-xs padding-top-xl">平台在每周六进行统一集中结算。只需填写支付宝收款账号，便可当天收到结算金额。</view>
						</view>
					</view>
				</view>
			</view>
		<view class="solids-bottom bg-yellow padding-xs flex align-center">
			
			<view class="flex-sub text-center">
				<view class="solid-bottom text-xl padding">
					<text class="text-black text-bold">现在就开启内容变现之旅</text>
				</view>
				<view class="padding flex flex-direction">
					<button class="cu-btn bg-black lg">成为商家</button>
					
				</view>
			</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.title{
			line-height: 2;
		}
</style>
