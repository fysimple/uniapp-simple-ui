<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	@import '@/common/sass/_reset.scss';
	@import '@/common/sass/_flexible.scss';
	@import '@/common/sass/_colors.scss';
	@import '@/common/sass/_fonts.scss';
	@import '@/common/sass/_spacing.scss';
	@import '@/common/sass/_buttons.scss';
	page{
		font-family:-apple-system,Source Sans Pro,Helvetica Neue,Arial,sans-serif;
		font-size: $uni-font-size-base;
		color: $uni-text-color;
		background-color: $uni-bg-color;
		transition: all .3s ease;
		overscroll-behavior: none;
	}
</style>
