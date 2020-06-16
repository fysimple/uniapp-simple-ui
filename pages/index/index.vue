<template>
	<view class="page-container">
		<styles class="page-content" v-if="tabId === 0"></styles>
		<algorithm class="page-content" v-else-if="tabId === 1"></algorithm>
		<animation class="page-content" v-else-if="tabId === 2"></animation>
		<question class="page-content" v-else></question>
		<tabbars @change="jump" class="g-tabbar-content"></tabbars>
	</view>
</template>

<script>
	import tabbars from "../../components/tabbars/tabbars.vue";
	import styles from '../../pages-style/index/index.vue';
	import algorithm from '../../pages-algorithm/index/index';
	import question from '../../pages-question/index/index';
	import animation from '../../pages-animation/index/index';
	export default {
		data() {
			return {
				tabId:0
			}
		},
		components:{
				tabbars,
				styles,
				algorithm,
				question,
				animation
		},
		onLoad() {

		},
		methods: {
			jump(index){
				if(index === this.tabId) return;
				this.tabId = index;
			}
		}
	}
</script>
<style lang="scss">
	.page-content{
		padding-bottom:calc(env(safe-area-inset-bottom) + #{$tabbar-height} + #{$uni-spacing-col-sm})
	}
	.g-tabbar-content{
		position: fixed;
		bottom: env(safe-area-inset-bottom);
		left: 0;
		right: 0;
		height: $tabbar-height;
	}
</style>
