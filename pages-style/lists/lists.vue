<template>
	<view>
		<view class="com-title box-mg-spacing">列表</view>
		<view class="flex list-item box-pd-spacing" v-for="(item,index) in listsData" :key="index">
			<image :src="item.image" mode="aspectFill"></image>
			<view class="flex-flex_1">
				<view class="com-text-ellipsis">{{item.name}}</view>
				<view class="font-size-sm text-color-grey mg-top-sm">{{item.describe}}</view>
				<view class="font-size-sm text-color-grey mg-top-sm text-color-red">{{item.describe2}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				listsData:[{
					image:'../../static/default.jpg',
					name:'列表项名称；单行省略;我的拽拽',
					describe:'列表项的描述，一般2行；我们家狗狗的名字',
					describe2:'uniapp 图片要记得设置宽度和高度，否则加载时会有拉伸问题！！'
				},
				{
					image:'../../static/default.jpg',
					name:'列表项名称；单行省略;我的拽拽',
					describe:'列表项的描述，一般2行；我们家狗狗的名字',
					describe2:'设置行高时，要记得减去行高内间距问题，否则和设计稿存在差入；不设置行高时，在小程序会出现，文字底边显示不出来问题！'
				},
				{
					image:'../../static/default.jpg',
					name:'列表项名称；单行省略;我的拽拽',
					describe:'列表项的描述，一般2行；我们家狗狗的名字'
				}]
			};
		}
	}
</script>

<style lang="scss">
	page{
		background-color: $uni-bg-color;
	}
	.list-item{
		background-color:#FFFFFF;
		image{
			margin-right: $uni-spacing-col-base;
			width: $uni-list-image-w;
			height: $uni-list-image-h;
			border-radius: $uni-list-image-radius;
		}
		& + .list-item{
			border-top: 1rpx solid $uni-border-color;
		}
	}
</style>
