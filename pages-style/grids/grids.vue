<template>
	<view>
		<view class="box-mg-spacing">
			<view class="com-title">九宫格</view>
			<view class="text-color-grey">flex布局；css新出了Grid属性，但兼容性太差；放弃table标签，是因为table标签的渲染，有时会出现大片空白！</view>
		</view>
		<!-- 无边框/九宫格 -->
		<view class="bg-color-white">
			<view class="box-pd-spacing text-color-grey bottom-border-line">无边框/九宫格</view>
			<view class="flex flex_col3 text-center">
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item1</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item2</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item3</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item4</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item5</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item6</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item7</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item8</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item9</view>
				</view>
			</view>
		</view>
		<!-- 有边框/九宫格 -->
		<view class="bg-color-white mg-top-base">
			<view class="box-pd-spacing text-color-grey">有边框/九宫格</view>
			<view class="flex flex_col3 text-center flex-grid_border">
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item1</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item2</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item3</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item4</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item5</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item6</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item7</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item8</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item9</view>
				</view>
			</view>
		</view>
		<!--  无边框/4列 -->
		<view class="bg-color-white mg-top-base">
			<view class="box-pd-spacing text-color-grey bottom-border-line">无边框/4列</view>
			<view class="flex flex_col4 text-center">
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item1</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item2</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item3</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item4</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item5</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item6</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item7</view>
				</view>
				<view class="flex-item">
					<custom-icons size="36" class="text-color-grey">&#xe644;</custom-icons>
					<view class="mg-top-base">item8</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import customIcons from '@/components/custom-icons/custom-icons.vue';
	export default {
		data() {
			return {
				
			}
		},
		components:{
			customIcons
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.bottom-border-line{
		border-bottom: 1rpx solid $uni-border-color;
	}
	.flex{
		&-item{
			padding: $uni-spacing-col-xl $uni-spacing-col-base;
			box-sizing: border-box;
		}
	}
</style>
