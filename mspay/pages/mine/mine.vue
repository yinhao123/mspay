<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">个人中心</block>
		</cu-custom>
		<view class="list cu-bar bg-white solid-bottom margin-top">
			<view class="action">
				<text class="cuIcon-title text-red "></text> 通用信息
			</view>
		</view>
		
		<view class="cu-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goUserInfo">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">个人资料</text>
				</view>
			</view>
			
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">系统设置</text>
				</view>
			</view>
		</view>
		
		
		<view class=" cu-bar bg-white solid-bottom margin-top">
			<view class="action">
				<text class="cuIcon-title text-orange "></text> 我是买家
			</view>
		</view>
		<view class="cu-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">已购商品</text>
				</view>
			</view>
			
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">我的售后</text>
				</view>
			</view>
		</view>
		<view class="cu-bar bg-white solid-bottom margin-top">
			<view class="action">
				<text class="cuIcon-title text-blue "></text> 我是卖家
			</view>		
		</view>
		<view class="cu-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goWallet">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">我的钱包</text>
				</view>
			</view>
		
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">商品列表</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goGoodsAdd">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">添加商品</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">订单管理</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-circlefill text-grey"></text>
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
			goGoodsAdd:function(){
				uni.navigateTo({
					url: "../seller/goodsAdd/goodsAdd"
				})
			},
			goUserInfo:function(){
				// 跳转到我的信息
				uni.navigateTo({
					url: "userInfo/userInfo"
				})
			},
			goWallet: function() {
				// 跳转到我的钱包
				uni.navigateTo({
					url: "wallet/wallet"
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

	.title {
		line-height: 2;
	}
</style>
