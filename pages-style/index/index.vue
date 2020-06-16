<template>
	<view>
		<!-- part 1 -->
		<view class="top">
			<view class="flex v-center">
				<!-- <image class="user-logo" src="https://qianxun-1300724986.cos.ap-chengdu.myqcloud.com/default/user-default.jpeg" mode="aspectFill"></image> -->
				<view class="flex-flex_1 flex-item">
					<view class="name font-size-lg">SIMPLE UI DEMO</view>
					<view class="describe font-size-base mg-top-base">语法：VUE；框架：UNI-APP；样式：CSS SElF</view>
					<view class="describe font-size-base mg-top-base">手机端常用样式、滑动、标签、列表、九宫格</view>
				</view>
			</view>
		</view>
		<!-- part 2 -->
		<view class="grid-wrapper com-box-spacing">
			<view class="flex flex-align_center flex-wrap_wrap">
				<view class="flex-flex_1 flex-item" @tap="onLink('colors/colors')">
					<image class="imgs" src="../static/menu-color.png" mode="aspectFill"></image>
					<view class="font-size-base">主题色</view>
				</view>
				<view class="flex-item line"></view>
				<view class="flex-item flex-flex_1" @tap="onLink('fonts/fonts')">
					<image class="imgs" src="../static/menu-font.png" mode="aspectFill"></image>
					<view class="font-size-base">字体大小</view>
				</view>
			</view>
		</view>
		<!-- part 3 -->
		<view class="font-size-lg title-spacing title-color">基础样式</view>
		<view class="basic-lists com-box-spacing">
			<block v-for="(item,index) in basicData" :key="index">
				<view class="flex-item flex flex-align_center" @tap="onLink(item.link)">
					<view class="icon-color" :class="item.color">
						<custom-icons class="block" size="40" v-html="item.icon"></custom-icons>
					</view>
					<text>{{item.title}}</text>
				</view>
			</block>
		</view>
	</view>
</template>

<script>
	import CustomIcons from '@/components/custom-icons/custom-icons.vue';
	export default {
		data() {
			return {
				basicData:[
					{
						icon:'&#xe602;',
						title:'图标-[ICON]',
						color:'pink',
						link:'icons/icons'
					},
					{
						icon:'&#xe63c;',
						title:'按钮-[BUTTON]',
						color:'primary',
						link:'buttons/buttons'
					},
					{
						icon:'&#xe692;',
						title:'九宫格/栅栏-[FLEX/GRID]',
						color:'green',
						link:'grids/grids'
					},
					{
						icon:'&#xe601;',
						title:'列表-[LIST]',
						color:'yellow',
						link:'lists/lists'
					},
					{
						icon:'&#xe622;',
						title:'滑动切换-[SWIPER]',
						color:'red',
						link:'swiper/swiper'
					}
				]
			}
		},
		components:{
				CustomIcons	
		},
		onLoad() {

		},
		created() {
			uni.setNavigationBarTitle({
				title:'样式'
			})
		},
		methods: {
			onLink(value){
				uni.navigateTo({
					url:'/pages-style/'+value,
				})
			}
		}
	}
</script>

<style lang="scss" src="./index.scss"></style>
