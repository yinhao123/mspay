<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">卖家中心</block>
		</cu-custom>
		
		
		
		<view class="cu-list avatar-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goSellerguide">
					<text class="cuIcon-emoji text-grey"></text>
					<text class="text-grey">系统演示</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goWallet">
					<text class="cuIcon-moneybag text-grey"></text>
					<text class="text-grey">我的钱包</text>
				</view>
			</view>
					
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-list text-grey"></text>
					<text class="text-grey">商品列表</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goGoodsAdd">
					<text class="cuIcon-roundadd text-grey"></text>
					<text class="text-grey">添加商品</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-form text-grey"></text>
					<text class="text-grey">订单管理</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-notice text-grey"></text>
					<text class="text-grey">投诉管理</text>
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
			goSellerguide:function(){
				uni.navigateTo({
					url: "../../context/context"
				})
			},
			goGoodsAdd:function(){
				uni.navigateTo({
					url: "../../seller/goodsAdd/goodsAdd"
				})
			},
			goUserInfo:function(){
				// 跳转到我的信息
				uni.navigateTo({
					url: "../userInfo/userInfo"
				})
			},
			goWallet: function() {
				// 跳转到我的钱包
				uni.navigateTo({
					url: "../wallet/wallet"
				})
			},
			
			goSaleList: function() {
				uni.navigateTo({
					url: "../list/list"
				})
			},
			goComplaintList:function(){
				uni.navigateTo({
					url: "application/complaintList/complaintList"
				})
			}
		}
	}
</script>

<style>
	.list {
		margin-top: 80upx;
	}
	.avatar-list {
		margin-top:80upx;
	}
	.title {
		line-height: 2;
	}
</style>
