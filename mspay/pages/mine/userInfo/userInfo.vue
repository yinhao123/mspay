<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">个人资料</block>
		</cu-custom>
		<!-- 用户个人信息页面 -->
		<view class="cu-list margin-top-xl menu-avatar">
		<view class="cu-item ">
			<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
			<view class="content">
				<view class="text-pink"><view class="text-cut">用户名称</view></view>
				<view class="text-gray text-sm flex"> <view class="text-cut">用户介绍</view></view>
			</view>
		</view>
		</view>
		<view class="cu-list menu">
			<view class="cu-item arrow">
				<view class="content" @tap="goSaleList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">用户名称</text>
				</view>
			</view>
			
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">实名认证</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content" @tap="goComplaintList">
					<text class="cuIcon-circlefill text-grey"></text>
					<text class="text-grey">手机号码</text>
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
