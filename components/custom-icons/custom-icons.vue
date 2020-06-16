<template>
	<text class="icons" :style="{fontSize:size + 'rpx'}">
		<slot></slot>
	</text>
</template>

<script>
	export default {
		props:{
			content:{
				type:String,
				default:''
			},
			size:{
				type:[Number,String],
				default:28
			}
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	@font-face {
	  font-family: 'iconfont';  /* project id 1779177 */
	  src: url('https://at.alicdn.com/t/font_1779177_okv1wl670vg.eot');
	  src: url('https://at.alicdn.com/t/font_1779177_okv1wl670vg.eot?#iefix') format('embedded-opentype'),
	  url('https://at.alicdn.com/t/font_1779177_okv1wl670vg.woff2') format('woff2'),
	  url('https://at.alicdn.com/t/font_1779177_okv1wl670vg.woff') format('woff'),
	  url('https://at.alicdn.com/t/font_1779177_okv1wl670vg.ttf') format('truetype'),
	  url('https://at.alicdn.com/t/font_1779177_okv1wl670vg.svg#iconfont') format('svg');
	}
	.icons{
		font-family:'iconfont';
		font-style: normal;
		-webkit-font-smoothinng:antialiased;
		-moz-osx-font-smoothing: grayscale;
	}
</style>
