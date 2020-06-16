<template>
	<view>
		<view class="com-title box-mg-spacing">Button 按钮</view>
		<view class="box-pd-spacing bg-color-white">
			<view class="title text-color-grey">【长-实心】图标的几种形式：图标按钮、禁用按钮、弧度大小、背景颜色、空心/实心、有/无背景等...</view>
			<custom-buttons class="mg-top-base"
							:className="'bg-color-primary custom-btn_round'"
							:size="'normal'">
							实心按钮
			</custom-buttons>
			<custom-buttons class="mg-top-base" 
							:className="'bg-color-primary'"
							:size="'normal'"
							:radius="12">
							实心按钮
			</custom-buttons>
			<custom-buttons class="mg-top-base" 
							:className="'bg-color-red'"
							:size="'normal'"
							:radius="12"
							>
				<custom-icons size="32" class="icons icons_bottom">&#xe603;</custom-icons>删除
			</custom-buttons>
			<custom-buttons :disabled="true" 
							class="mg-top-base" 
							:className="'bg-color-primary'"
							:size="'normal'"
							:radius="12"
							>禁用按钮
			</custom-buttons>
		</view>
		<view class="box-pd-spacing bg-color-white mg-top-base">
			<view class="title text-color-grey">【长-空心】:带图标、禁用的按钮，设置默认的宽、高、字体大小、颜色</view>
			<custom-buttons class="mg-top-base"
							:className="'custom-btn-border custom-btn_round border-color-primary text-color-primary'"
			>空心按钮</custom-buttons>
			<custom-buttons class="mg-top-base"
							:className="'custom-btn-border border-color-primary text-color-primary'"
							:radius="0"
			>空心按钮</custom-buttons>
			<custom-buttons class="mg-top-base"
							:className="'custom-btn-border text-color-red border-color-red'"
							:size="'normal'"
							:radius="0"
							>
				<custom-icons size="32" class="icons icons_bottom">&#xe603;</custom-icons>删除
			</custom-buttons>
			<custom-buttons :disabled="true"
							class="mg-top-base"
							:size="'normal'"
							:radius="0"
							:className="'custom-btn-border border-color-primary text-color-primary'"
			>空心按钮</custom-buttons>
		</view>
		<view class="box-pd-spacing bg-color-white mg-top-base">
			<view class="title text-color-grey">【小-实心/空心】</view>
			<view>
				<custom-buttons class="mg-top-base"
								:className="'custom-btn-border border-color-primary text-color-primary'"
								:size="'small'"
				>空心按钮</custom-buttons>
				<custom-buttons class="mg-top-base"
								:className="'custom-btn-border text-color-red border-color-red'"
								:size="'small'"
								>
					<custom-icons size="32" class="icons icons_bottom">&#xe603;</custom-icons>删除
				</custom-buttons>
				<custom-buttons :disabled="true"
								class="mg-top-base"
								:className="'custom-btn-border border-color-primary text-color-primary'"
								:size="'small'"
				>空心按钮</custom-buttons>
			</view>
			<view class="mg-top-base">
				<custom-buttons :className="'bg-color-primary text-color-white'"
								:size="'small'"
								:radius="8">
								实心按钮
				</custom-buttons>
				<custom-buttons :className="'bg-color-red text-color-white'"
								:size="'small'"
								:radius="8"
								>
					<custom-icons size="32" class="icons icons_bottom">&#xe603;</custom-icons>删除
				</custom-buttons>
				<custom-buttons :disabled="true" 
								:className="'bg-color-primary text-color-white'"
								:size="'small'"
								:radius="8"
								>禁用按钮
				</custom-buttons>
			</view>
			<view class="mg-top-base">
				<custom-buttons :className="'bg-color-primary text-color-white custom-btn_round'"
								:size="'small'">
								实心按钮
				</custom-buttons>
				<custom-buttons :className="'bg-color-red text-color-white custom-btn_round'"
								:size="'small'"
								>
					<custom-icons size="32" class="icons icons_bottom">&#xe603;</custom-icons>删除
				</custom-buttons>
				<custom-buttons :disabled="true" 
								:className="'bg-color-primary text-color-white custom-btn_round'"
								:size="'small'"
								>禁用按钮
				</custom-buttons>
			</view>
		</view>
	</view>
	
</template>

<script>
	import customButtons from '@/components/custom-buttons/custom-buttons.vue';
	import CustomIcons from '@/components/custom-icons/custom-icons.vue';
	export default {
		data() {
			return {
				
			};
		},
		components:{
			customButtons,
			CustomIcons
		}
	}
</script>

<style lang="scss">
	.custom-btn-normal{
		width: 100%;
	}
	.custom-btn-small{
		margin-right: $uni-spacing-col-base;
		min-width: 200rpx;
	}
</style>
