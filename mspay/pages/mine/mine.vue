<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">个人中心</block>
		</cu-custom>
		<view class="cu-list avatar-list margin-top-xl menu-avatar">
		<view class="cu-item ">
			<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
			<view class="content">
				<view class="text-pink"><view class="text-cut">用户名称</view></view>
				<view class="text-gray text-sm flex"> <view class="text-cut">用户介绍</view></view>
			</view>
		</view>
		</view>
		<!-- <view class=" cu-bar bg-white solid-bottom margin-top">
			<view class="action">
				<text class="cuIcon-title text-red "></text> 通用信息
			</view>
		</view> -->
		
		<view class="cu-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goUserInfo">
					<text class="cuIcon-profile text-grey"></text>
					<text class="text-grey">个人资料</text>
				</view>
			</view>
			
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-settings text-grey"></text>
					<text class="text-grey">系统设置</text>
				</view>
			</view>
		</view>

		<view class="cu-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-cart text-grey"></text>
					<text class="text-grey">已购商品</text>
				</view>
			</view>
			
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-favor text-grey"></text>
					<text class="text-grey">我的售后</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="gosellerCenter">
					<text class="cuIcon-selection text-grey"></text>
					<text class="text-grey">卖家中心</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-service text-grey"></text>
					<text class="text-grey">在线服务</text>
				</view>
			</view>
		</view>
		
		<view class="padding-xs flex align-center">
			
			<view class="flex-sub text-center">
				<view class="solid-bottom text-xs yuezhifu-footer padding">
					<text class="text-gray">悦知付©2016-2019 </text>
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
			gosellerCenter:function(){
				uni.navigateTo({
					url: "sellerCenter/sellerCenter"
				})
			},
			goSellerguide:function(){
				uni.navigateTo({
					url: "../context/context"
				})
			},
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
		
	.yuezhifu-footer {
		margin-top:200upx;
	}
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
