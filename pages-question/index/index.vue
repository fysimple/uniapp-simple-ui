<template>
	<view>
		<view class="com-title box-mg-spacing">问题分类</view>
		<view class="font-size-sm text-color-grey box-mg-spacing">前端问题：主要包括HTML（标签语义化、H5标签等）、CSS（新属性的使用、定位、浮动、清除浮动、动画效果以及各个浏览器的兼容问题）、
		JAVASCRIPT(语法、ES6、WEB API)、VUE（...）、REACT（...），后期会添加一些小程序的常用框架...未完待续...</view>
		<view class="list-wrapper">
			<view class="com-box-spacing"></view>
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
	
</style>
