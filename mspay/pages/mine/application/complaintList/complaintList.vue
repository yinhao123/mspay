<template>
	<view>
		<!-- 投诉列表 -->
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">我的售后</block>
		</cu-custom>
		<view class="cu-list menu-avatar">
		<view class="cu-item " @tap="goResult">
			<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
			<view class="content">
				<view class="text-pink"><view class="text-cut">文件名称</view></view>
				<view class="text-gray text-sm flex"> <view class="text-cut">文件简介，截取前50个字。。。。。</view></view>
			</view>
			<view class="action">
				<view class="text-grey text-xs">销量:10</view>
				<view class="cu-tag round bg-red sm">￥5</view>
			</view>
		</view>
		<view class="cu-item ">
			<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
			<view class="content">
				<view class="text-pink"><view class="text-cut">文件名称</view></view>
				<view class="text-gray text-sm flex"> <view class="text-cut">文件简介，截取前50个字。。。。。</view></view>
			</view>
			<view class="action">
				<view class="text-grey text-xs">销量:10</view>
				<view class="cu-tag round bg-red sm">￥5</view>
			</view>
		</view>
		<view class="cu-item ">
			<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
			<view class="content">
				<view class="text-pink"><view class="text-cut">文件名称</view></view>
				<view class="text-gray text-sm flex"> <view class="text-cut">文件简介，截取前50个字。。。。。</view></view>
			</view>
			<view class="action">
				<view class="text-grey text-xs">销量:10</view>
				<view class="cu-tag round bg-red sm">￥5</view>
			</view>
		</view>
		<view class="cu-item ">
			<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
			<view class="content">
				<view class="text-pink"><view class="text-cut">文件名称</view></view>
				<view class="text-gray text-sm flex"> <view class="text-cut">文件简介，截取前50个字。。。。。</view></view>
			</view>
			<view class="action">
				<view class="text-grey text-xs">销量:10</view>
				<view class="cu-tag round bg-red sm">￥5</view>
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
			goResult:function(){
				uni.navigateTo({
					url:"../result/result"
				})
			}
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
