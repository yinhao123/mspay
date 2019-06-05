<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<!-- 	<block slot="backText">返回</block> -->
			<block slot="content">悦知付</block>
		</cu-custom>
		<view class="margin-top-xl">
			<view class="solids-bottom padding-xs flex align-center">

				<view class="flex-sub text-center">
					<view class="solid-bottom text-lg padding">
						<text class="text-black">知识付费样例</text>
					</view>
				</view>
			</view>
			
			
			
			<view class="uni-common-mt" style="background:#FFF; padding:20upx;">
                <rich-text :nodes="nodes"></rich-text>
            </view>


			<view class="padding-xl bg-white solid-bottom" >
				<view class="text-left">商品序号：1586</view>
				<view class="text-left">作者姓名：张三</view>
				<view class="text-left">芝麻信用：优秀</view>
				<view class="text-left">发布时间：2019-06-05</view>
				<view class="text-left">付费人数：51</view>
			</view>
			<view class="padding bg-white solid-bottom" >
				
				<view class="text-center ">以下为付费内容,请支付后查看</view>
				
			</view>
		
			
			
			
			<view v-if="canSeeContext" class="bg-img bg-mask flex  justify-center" style="background-image: url('https://ossweb-img.qq.com/images/lol/web201310/skin/big10006.jpg');height: 400upx;">
			
				<view class="padding-xl justify-center flex text-white">
					
					<view class="padding flex flex-direction">
						<view class="  flex align-center">
							
							<view class="flex-sub text-center">
								<view class="text-xxl ">
									<text class="text-price  text-red">1.00</text>
								</view>
							</view>
						</view>
						<view class="padding " >							
							<view class="text-center"><text class="cuIcon-lock">隐藏内容 支付可见</text></view>
						</view>
						<button @tap="seeContext" class="cu-btn bg-blue lg">立即支付</button>
					</view>
				</view>
			</view>
			
			<view v-else="canSeeContext">隐藏内容：XXXXXXXXXXXXXXXXX
				<button @tap="copyContext">复制</button>
			</view>

			


		</view>
		
		<view class="solids-bottom padding-xs flex align-center">
			
			<view class="flex-sub text-center">
				<view class="solid-bottom text-sm padding text-blue">
					<text @tap="goHelpPage" class="text-grey ">使用帮助</text>
					<text @tap = "goInfringement" class="text-grey padding">侵权投诉</text>
					<text @tap="goSellerguide" class="text-grey">成为卖家</text>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				canSeeContext: true,
				context: '加密隐藏内容',
				isLogin: false
			}
		},
		onLoad: function() {

		},
		methods: {
			goInfringement:function(){
				uni.showModal({
					title: '悦知付提示',
					content: '请发邮件至service@yuezhipay.com',
					success: function (res) {
						if (res.confirm) {
							console.log('用户点击确定');
						} else if (res.cancel) {
							console.log('用户点击取消');
						}
					}
				});
			},
			goHelpPage:function(){
				uni.navigateTo({
					url: "../help/help"
				})
			},
			goSellerguide:function(){
					uni.navigateTo({
						url: "../sellerguide/sellerguide"
					})
				},
			backIndex: function() {
				// 返回介绍界面
				uni.navigateTo({
					url: "../index/index"
				})
			},
			seeContext: function() {
				if (!this.isLogin) {
					// 先登陆
					uni.showModal({
						title: '系统提示',
						content: '请先登陆',
						success: function(res) {
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
			copyContext: function() {
				// 将加密内容复制到剪贴板上
				uni.setClipboardData({
					data: '复制成功',
					success: function() {
						console.log('success');
					}
				});
			}
		}
	}
</script>

<style>
	.title {
		line-height: 2;
	}
	
</style>
