<template>
	<view class="tabbar-wrapper text-center flex-justify_center flex-align_center flex bg-color-white">
		<view class="flex-item flex-flex_1 active" v-for="(item,index) in tabDatas" :key="index" @tap="onChange(index)">
			<image mode="aspectFill" :src="item.imgActive"></image>
			<view :style="{'color':setColors(index)}">{{item.name}}</view>
		</view>
	</view>
</template>

<script>
	import CustomIcons from "../custom-icons/custom-icons.vue";
	export default {
		props:{
			index:{
				type:Number,
				default:0
			}
		},
		data() {
			return {
				tabId:0,
				tabDatas:[{
					imgActive:'../../static/tabbar/tabbar-item-active-01.png',
					name:'样式'
				},
				{
					imgActive:'../../static/tabbar/tabbar-item-active-03.png',
					name:'算法'
				},
				{
					imgActive:'../../static/tabbar/tabbar-item-active-02.png',
					name:'动画'
				},
				{
					imgActive:'../../static/tabbar/tabbar-item-active-04.png',
					name:'问题'
				}
				]
			}
		},
		methods: {
			onChange(index){
				this.tabId = index;
				// 调用父类的方法
				this.$emit('change',index)
			},
			setColors(index){
				if(this.tabId !== index) return '';
				let str = '';
				switch(index){
					case 0:
						str = '#6aacfc';
						break;
					case 1:
						str = '#96a1f7';
						break;
					case 2:
						str = '#fb927a';
						break;	
					default:
						str = '#f5a623';
						break;
				}
				return str;
			}
		},
		components:{
			CustomIcons
		}
	}
</script>

<style lang="scss">
	.tabbar-wrapper{
		.item{
			font-size: $uni-font-size-sm;
		}
		image{
			margin: auto auto 5rpx;
			display: block;
			width: 45rpx;
			height: 45rpx;
		}
	}
</style>
