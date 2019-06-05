<template>
	<view>
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">商品列表</block>
		</cu-custom>

		<view class="cu-list menu-avatar">
			<view class="cu-item" :class="modalName=='move-box-'+ index?'move-cur':''" v-for="(item,index) in 4" :key="index"
			 @touchstart="ListTouchStart" @touchmove="ListTouchMove" @touchend="ListTouchEnd" :data-target="'move-box-' + index">
				<view class="cu-avatar round lg" :style="[{backgroundImage:'url(https://ossweb-img.qq.com/images/lol/web201310/skin/big2100'+ (index+2) +'.jpg)'}]"></view>
				<view class="content">
					<view class="text-grey">XXX</view>
					<view class="text-gray text-sm">
						<text class="cuIcon-infofill text-red  margin-right-xs"></text> 消息未送达</view>
				</view>
				<view class="action">
					<view class="text-grey text-xs">22:20</view>
					<view class="cu-tag round bg-grey sm">5</view>
				</view>
				<view class="move">
					<view class="bg-grey" @tap="goGoodsEdit">编辑</view>
					<view class="bg-red" @tap="deleteComfirm">删除</view>
				</view>
			</view>
		</view>

		<view class="cu-list menu-avatar">
			<view class="cu-item ">
				<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
				<view class="content">
					<view class="text-pink">
						<view class="text-cut">文件名称</view>
					</view>
					<view class="text-gray text-sm flex">
						<view class="text-cut">文件简介，截取前50个字。。。。。</view>
					</view>
				</view>
				<view class="action">
					<view class="text-grey text-xs">销量:10</view>
					<view class="cu-tag round bg-red sm">￥5</view>
				</view>
			</view>
			<view class="cu-item ">
				<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
				<view class="content">
					<view class="text-pink">
						<view class="text-cut">文件名称</view>
					</view>
					<view class="text-gray text-sm flex">
						<view class="text-cut">文件简介，截取前50个字。。。。。</view>
					</view>
				</view>
				<view class="action">
					<view class="text-grey text-xs">销量:10</view>
					<view class="cu-tag round bg-red sm">￥5</view>
				</view>
			</view>
			<view class="cu-item ">
				<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
				<view class="content">
					<view class="text-pink">
						<view class="text-cut">文件名称</view>
					</view>
					<view class="text-gray text-sm flex">
						<view class="text-cut">文件简介，截取前50个字。。。。。</view>
					</view>
				</view>
				<view class="action">
					<view class="text-grey text-xs">销量:10</view>
					<view class="cu-tag round bg-red sm">￥5</view>
				</view>
			</view>
			<view class="cu-item ">
				<view class="cu-avatar radius lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png);"></view>
				<view class="content">
					<view class="text-pink">
						<view class="text-cut">文件名称</view>
					</view>
					<view class="text-gray text-sm flex">
						<view class="text-cut">文件简介，截取前50个字。。。。。</view>
					</view>
				</view>
				<view class="action">
					<view class="text-grey text-xs">销量:10</view>
					<view class="cu-tag round bg-red sm">￥5</view>
				</view>
			</view>
		</view>
		<view class="padding-xs flex align-center">

			<view class="flex-sub text-center">
				<view class=" text-xs padding">
					<text class="text-gray">Tips:右滑可对商品进行编辑和删除操作</text>
				</view>

			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				cuIconList: [{
					cuIcon: 'cardboardfill',
					color: 'red',
					badge: 120,
					name: 'VR'
				}, {
					cuIcon: 'recordfill',
					color: 'orange',
					badge: 1,
					name: '录像'
				}, {
					cuIcon: 'picfill',
					color: 'yellow',
					badge: 0,
					name: '图像'
				}, {
					cuIcon: 'noticefill',
					color: 'olive',
					badge: 22,
					name: '通知'
				}, {
					cuIcon: 'upstagefill',
					color: 'cyan',
					badge: 0,
					name: '排行榜'
				}, {
					cuIcon: 'clothesfill',
					color: 'blue',
					badge: 0,
					name: '皮肤'
				}, {
					cuIcon: 'discoverfill',
					color: 'purple',
					badge: 0,
					name: '发现'
				}, {
					cuIcon: 'questionfill',
					color: 'mauve',
					badge: 0,
					name: '帮助'
				}, {
					cuIcon: 'commandfill',
					color: 'purple',
					badge: 0,
					name: '问答'
				}, {
					cuIcon: 'brandfill',
					color: 'mauve',
					badge: 0,
					name: '版权'
				}],
				modalName: null,
				gridCol: 3,
				gridBorder: false,
				menuBorder: false,
				menuArrow: false,
				menuCard: false,
				skin: false,
				listTouchStart: 0,
				listTouchDirection: null,
			};
		},
		methods: {
			goGoodsEdit: function() {
				uni.navigateTo({
					url: "../seller/goodsEdit/goodsEdit"
				})
			},
			deleteComfirm: function() {
				uni.showModal({
					title: '删除提示',
					content: '确定到删除这个商品吗？',
					success: function(res) {
						if (res.confirm) {
							console.log('用户点击确定');
						} else if (res.cancel) {
							console.log('用户点击取消');
						}
					}
				});
			},
			showModal(e) {
				this.modalName = e.currentTarget.dataset.target
			},
			hideModal(e) {
				this.modalName = null
			},
			Gridchange(e) {
				this.gridCol = e.detail.value
			},
			Gridswitch(e) {
				this.gridBorder = e.detail.value
			},
			MenuBorder(e) {
				this.menuBorder = e.detail.value
			},
			MenuArrow(e) {
				this.menuArrow = e.detail.value
			},
			MenuCard(e) {
				this.menuCard = e.detail.value
			},
			SwitchSex(e) {
				this.skin = e.detail.value
			},

			// ListTouch触摸开始
			ListTouchStart(e) {
				this.listTouchStart = e.touches[0].pageX
			},

			// ListTouch计算方向
			ListTouchMove(e) {
				this.listTouchDirection = e.touches[0].pageX - this.listTouchStart > 0 ? 'right' : 'left'
			},

			// ListTouch计算滚动
			ListTouchEnd(e) {
				if (this.listTouchDirection == 'left') {
					this.modalName = e.currentTarget.dataset.target
				} else {
					this.modalName = null
				}
				this.listTouchDirection = null
			}
		}
	}
</script>

<style>
	.cu-list {
		margin-top: 80upx;
	}

	.title {
		line-height: 2;
	}
</style>
