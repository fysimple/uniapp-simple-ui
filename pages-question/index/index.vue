<template>
	<view>
		<view class="com-title box-mg-spacing">问题分类</view>
		<view class="font-size-sm text-color-grey page-sub-title">VUE、路由、VUEX、面试题</view>
		<view class="list-wrapper">
			<view class="flex flex_col3">
				<view class="flex-item">
					<view class="cont">VUE</view>
				</view>
				<view class="flex-item">
					<view class="cont">V路由</view>
				</view>
				<view class="flex-item">
					<view class="cont">VUEX</view>
				</view>
				<view class="flex-item">
					<view class="cont">V面试题</view>
				</view>
			</view>
		</view>
		<view class="font-size-sm text-color-grey page-sub-title">HTML的属性、标签、进阶、面试题</view>
		<view class="list-wrapper">
			<view class="flex flex_col3">
				<view class="flex-item">
					<view class="cont">H属性</view>
				</view>
				<view class="flex-item">
					<view class="cont">H标签</view>
				</view>
				<view class="flex-item">
					<view class="cont">H进阶</view>
				</view>
				<view class="flex-item">
					<view class="cont">H面试题</view>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		created() {
			uni.setNavigationBarTitle({
				title:'问题'
			})
		},
	}
</script>

<style lang="scss">
	.page-sub-title{
		margin: auto $uni-spacing-col-lg $uni-spacing-col-lg;
	}
	.list-wrapper{
		margin: auto $uni-spacing-col-lg - $uni-spacing-col-base auto $uni-spacing-col-lg;
	}
	.flex-item{
		padding-right: $uni-spacing-col-base;
		.cont{
			font-size: $uni-font-size-sm;
			font-weight: 500;
			line-height: 100rpx;
			text-align: center;
			background-color: rgba($color: $uni-color-primary, $alpha: .1);
			box-shadow: $box-shadow;
			border-radius: 12rpx;
		}
	}
</style>
