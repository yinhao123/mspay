<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">我的钱包</block>
		</cu-custom>
		
		<view>
			<view class="cuIcon-moneybag"></view>
			<view>我的零钱</view>
			<view>￥0.0</view>
			<view>
				<button>提现</button>
				<view>查看账单详情</view>
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
		.cu-list {
			margin-top: 80upx;
		}
		.title{
			line-height: 2;
		}
</style>
