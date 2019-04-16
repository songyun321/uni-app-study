<template>
	<view>
		<!-- 搜索条 -->
		<view style="width:96%; padding:10upx 2%; background:	#1E90FF; flex-wrap:nowrap;">
		    <view class="grace-search">
		        <view class="grace-search-btns">
		            <image :src="staticUrl + 'scan.png'" mode='widthFix'></image>
		        </view>
		        <view class="grace-search-in">
		            <view class="grace-search-icon"></view>
		            <input type="search" @input="searchChange" @confirm="searchNow" :value="searchKey" placeholder="奔驰女主公开..."></input>
		            <view class="grace-search-icon grace-search-clear" @tap="clearKey" v-if="searchClose"></view>
		        </view>
		    </view>
		</view>
		<!-- 搜索条 -->
		
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

</style>
