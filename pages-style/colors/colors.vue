<template>
	<view class="box-mg-spacing pd-bottom-base">
		<block v-for="(item,index) in colorData" :key="index">
			<view class="com-title">{{item.title}}</view>
			<view class="text-color-grey">{{item.describe}}</view>
			<view class="box flex flex-wrap_wrap">
				<block v-for="(subItem,subIndex) in item.colorLists" :key="subIndex">
					<view class="flex-item mg-top-base" :class="subItem.bgClass">
						{{subItem.text}}
					</view>
				</block>
			</view>
		</block>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				colorData:[
					{
						title:'主题色',
						describe:'一个网站的标识色系以及和主题色相似的颜色！',
						colorLists:[
							{
								bgClass:'bg-color-primary',
								text:'颜色：#3f6ff1'
							},
							{
								bgClass:'bg-color-second-primary',
								text:'颜色：#344fea'
							}
						]
					},
					{
						title:'辅助色',
						describe:'区别于主题色，与主题色相匹配的其他颜色标识！',
						colorLists:[
							{
								bgClass:'bg-color-green',
								text:'颜色：#4bc124'
							},
							{
								bgClass:'bg-color-yellow',
								text:'颜色：#f5a623'
							},
							{
								bgClass:'bg-color-pink',
								text:'颜色：#fb927a'
							},
							{
								bgClass:'bg-color-red',
								text:'颜色：#cc0000'
							}
						]
					},
					{
						title:'字体颜色',
						describe:'常用的字体颜色',
						colorLists:[
							{
								bgClass:'bg-text-color',
								text:'基础色：#354052'
							},
							{
								bgClass:'bg-text-color-grey',
								text:'提示色：#999'
							},
							{
								bgClass:'bg-text-color-placeholder',
								text:'占位符：#808080'
							},
							{
								bgClass:'bg-text-color-disabled',
								text:'禁用色：#c0c0c0'
							}
						]
					},
					{
						title:'背景色/边框色',
						describe:'常用的背景色、边框色',
						colorLists:[{
								bgClass:'bg-color grey',
								text:'背景色：#f8f9f8'
							},
							{
								bgClass:'bg-color-border grey',
								text:'边框色：#efeef3'
							}
						]
					},
					{
						title:'遮罩层',
						describe:'常用的遮罩层',
						colorLists:[{
							bgClass:'bg-color-mask',
							text:'#000 alpha 40%'
						}]
					}
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #FFFFFF;
	}
	.box{
		margin-right: -$uni-spacing-col-base;
	}
	.flex-item{
		margin-right: $uni-spacing-col-base;
		flex-shrink: 0;
		width: 210rpx;
		height: 130rpx;
		font-size: $uni-font-size-sm;
		line-height: 130rpx;
		color: #FFFFFF;
		text-align: center;
		border-radius: 10rpx;
		&.grey{
			color: $uni-text-color-grey;
		}
	}
</style>
