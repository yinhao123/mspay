<template>
	<view>
			<cu-custom bgColor="bg-gradual-pink" :isBack="true"><block slot="backText">返回</block><block slot="content">时间轴</block></cu-custom>
	<view class="cu-timeline">
		<view class="cu-time">昨天</view>
		<view class="cu-item cur cuIcon-noticefill">
			<view class="content bg-green shadow-blur">
				<text>22:22</text> 【广州市】快件已到达地球
			</view>
		</view>
		<view class="cu-item text-red cuIcon-attentionforbidfill">
			<view class="content bg-red shadow-blur">
				这是第一次，我家的铲屎官走了这么久。久到足足有三天！！
			</view>
		</view>
		<view class="cu-item text-grey cuIcon-evaluate_fill">
			<view class="content bg-grey shadow-blur">
				这是第一次，我家的铲屎官走了这么久。
			</view>
		</view>
		<view class="cu-item text-blue">
			<view class="bg-blue content">
				<text>20:00</text> 【月球】快件已到达月球，准备发往地球
			</view>
			<view class="bg-cyan content">
				<text>10:00</text> 【银河系】快件已到达银河系，准备发往月球
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

</style>
