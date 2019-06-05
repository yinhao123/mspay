<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">我的钱包</block>
		</cu-custom>
		
		<view class="margin-top-xl padding-xs wallet-local flex align-center">
			
			<view class="flex-sub text-center">
				<view class=" text-sl padding">
					<text class=" cuIcon-moneybag text-yellow"></text>
				</view>
				<view class=" text-xxl padding">
					<text class="text-price text-red">80.00</text>
				</view>
				<view class=" text-sm padding">
					<text class="text-grey">待到账￥50.00</text>
				</view>
				
			</view>
		</view>
		
		<view>
			
			<view class="padding flex flex-direction">
				<button class="cu-btn bg-blue lg">提现</button>
			</view>
		</view>
		
		<view class=" padding-xs flex align-center">
			
			<view class="flex-sub text-center">
				<view class=" text-sm padding">
					<text class="text-grey">查看交易详情</text>
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
	.wallet-local{
		margin-top: 250upx;
	}
		.cu-list {
			margin-top: 80upx;
		}
		.title{
			line-height: 2;
		}
</style>
