<template>
	<view>
		<!-- 关于我们 -->
		<cu-custom class="title" bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">个人中心</block>
		</cu-custom>
		悦知付是一款什么样的产品呢？
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
.title {
		line-height: 2;
	}
</style>
