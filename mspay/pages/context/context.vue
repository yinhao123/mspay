<template>
	<view>
		
		<view>内容查看页</view>
		<view>作者：XXXX</view>
		<view>图文介绍</view>
		<view v-if="canSeeContext">
			<button @tap="seeContext">付费查看</button>
		</view>
		
		<view v-else="canSeeContext">隐藏内容：XXXXXXXXXXXXXXXXX
			<button @tap="copyContext">复制</button>
		</view>
		
		<view><button @tap="backIndex">马上赚钱</button></view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				canSeeContext: true,
				context:'加密隐藏内容',
				isLogin: false
			}
		},
		onLoad:function() {
	
		},
		methods: {
			backIndex:function(){
				// 返回介绍界面
				uni.navigateTo({
					url:"../index/index"
				})
			},
			seeContext:function () {
				if(!this.isLogin){
							// 先登陆
						uni.showModal({
						title: '系统提示',
						content: '请先登陆',
						success: function (res) {
							if (res.confirm) {
								console.log('用户点击确定');
								console.log(this.isLogin);
								this.isLogin = true;
								
							} else if (res.cancel) {
								console.log('用户点击取消');
							}
						}
					});
				}
				
				//判断是否可以查看加密内容，如果可以查看加密内容，则显示加密内容
				this.canSeeContext = !this.canSeeContext;
			},
			copyContext:function(){
				// 将加密内容复制到剪贴板上
				uni.setClipboardData({
						data: '复制成功',
						success: function () {
							console.log('success');
						}
					});
			}
		}
	}
</script>

<style>

</style>
