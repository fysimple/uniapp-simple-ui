<template>
	<view>
		<view class="com-title box-mg-spacing">
			icons 图标
		</view>
		<view class="box-pd-spacing bg-color-white" v-for="(item,index) in iconsData" :key="index">
			<view class="text-color-grey">{{item.title}}</view>
			<view class="flex_col3 flex">
				<view class="flex-item text-center" v-for="(subItem,subIndex) in item.lists" :key="subIndex">
					<custom-icons size="45" v-html="subItem.icons"></custom-icons>
					<view class="font-size-sm mg-top-base">{{subItem.name}}</view>
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
				iconsData:[
					{
						title:'常用/喜欢',
						lists:[{
							id:1,
							icons:'&#xe602;',
							name:'绘画：#xe602'
						},
						{
							id:2,
							icons:'&#xe63c;',
							name:'按钮：#xe63c'
						},
						{
							id:3,
							icons:'&#xe604;',
							name:'动画：#xe604'
						},
						{
							id:4,
							icons:'&#xe630;',
							name:'算法：#xe630'
						},
						{
							id:5,
							icons:'&#xe601;',
							name:'列表：#xe601'
						},
						{
							id:6,
							icons:'&#xe692;',
							name:'九宫格：#xe692'
						},
						{
							id:7,
							icons:'&#xe603;',
							name:'删除：#xe603'
						},
						{
							id:8,
							icons:'&#xe644;',
							name:'默认图：#xe644'
						},
						{
							id:9,
							icons:'&#xe622;',
							name:'swiper：#xe622'
						}]
					}
				]
			};
		},
		components:{
			customIcons
		}
	}
</script>

<style lang="scss">
	.flex-item{
		margin-top: 40rpx;
	}
</style>
