<template>
	<view>
		<view  class="shuru">
			<textarea  adjust-position="ture" placeholder="分享新鲜事" ></textarea>
			</view>
			<view class="xuanz">
				<image src="../../static/wo/jiu01.png"></image>
				<image src="../../static/xiezuo/at.png"></image>
				<image src="../../static/xiezuo/GIF.png"></image>
				
				<image src="../../static/xiezuo/xiaolianxiaolian.png"></image>
				<image src="../../static/xiezuo/jiahao.png"></image>
				
			</view>
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style>
	.shuru{height: 750upx; width: 750upx; background-color: 	#F0F8FF;}
	.shuru textarea{font-size: 30upx;}
	.xuanz{ display: flex; background-color: 	#F5DEB3; justify-content: space-between;}
	.xuanz image{width: 50upx; height: 50upx;}

</style>
