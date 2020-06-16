<template>
	<view class="box-mg-spacing">
		<view class="com-title">字体</view>
		<view class="row">
			<div class="item">Font Family</div>
			<div class="item text-color-grey mg-top-base">-apple-system</div>
		</view>
		<view class="com-title">字号</view>
		<view class="row flex flex-justify_center" v-for="(item,index) in fontSizeData" :key="index">
			<div class="flex-item flex-item_size" :class="item.textClass">{{item.textSize}}</div>
			<div class="flex-item flex-item_other">{{item.lineHeight}}</div>
			<div class="flex-item flex-item_other">{{item.textDescribe}}</div>
		</view>
	</view>

</template>

<script>
	export default {
		data() {
			return {
				fontSizeData:[{
					textClass:'font-size-xxl',
					textSize:'40PX',
					textDescribe:'仅用于数字',
					lineHeight:'line-height 60px,上下间距 -10PX',
				},
				{
					textClass:'font-size-xl',
					textSize:'36PX',
					textDescribe:'非常用字号，如大模块标题',
					lineHeight:'line-height 54px,上下间距 -9PX',
				},
				{
					textClass:'font-size-lg',
					textSize:'32PX',
					textDescribe:'常用字号，如常规标题',
					lineHeight:'line-height 48px,上下间距 -8PX',
				},
				{
					textClass:'font-size-base',
					textSize:'28PX',
					textDescribe:'常用字号，如正文/商品名称',
					lineHeight:'line-height 48px,上下间距 -7PX',
				},
				{
					textClass:'font-size-sm',
					textSize:'24PX',
					textDescribe:'常用字号，如辅助信息/注释',
					lineHeight:'line-height 36px,上下间距 -6PX',
				},
				{
					textClass:'font-size-xs',
					textSize:'20PX',
					textDescribe:'非常用字号，如标签',
					lineHeight:'line-height 30px,上下间距 -5PX',
				}]
			};
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #FFFFFF;
	}
	.flex-item{
		line-height: 1.5;
		text-align: left;
		&_size{
			flex-shrink: 0;
			width: 160rpx;
			margin-bottom: 40rpx;
			margin-right: 0;
			flex-shrink: 0;
		}
		&_other{
			flex-shrink: 0;
			flex: 1;
			padding-right: 40rpx;
			margin-bottom: 40rpx;
			font-size: $uni-font-size-sm;
			color: $uni-text-color-grey;
		}
	}
</style>
