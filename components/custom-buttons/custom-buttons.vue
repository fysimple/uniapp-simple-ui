<template>
	<button
			class="custom-btn"
			:class="[className,'custom-btn-'+ size]" 
			:disabled="disabled"
			:style="{'border-radius':radius + 'rpx'}">
		<slot></slot>
	</button>
</template>

<script>
	export default {
		props:{
			className:{
				type:String,
				default:''
			},
			disabled:{
				type:Boolean,
				default:false
			},
			size:{
				type:String,
				default:'normal'
			},
			radius:{
				type:[Number,String],
				default:''
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss"></style>
