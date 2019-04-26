<template>
	<!-- 主体 start -->
	<view class="index-body">
		<!-- 搜索框 -->
		<view class="grace-search-in" style="margin-top:10px;">
			<view class="grace-search-icon"></view>
			<input type="search" style="height:28upx; line-height:28upx; font-size:12px;" @input="searchChange" @confirm="searchNow" :value="searchKey" placeholder="9.9 包邮"></input>
		</view>
		<!-- 九宫格 start -->
		<view style="margin:20px 0;" class="grace-wrap">
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/1.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">美食</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/2.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">热销</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/3.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">超市</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/4.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">福利</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/5.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">免单</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/6.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">兑换</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/7.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">邀请</view>
			</view>
			<view class="grace-boxes">
				<view class="grace-boxes-img">
					<image src="../../static/indexcate/8.png" mode="widthFix"></image>
				</view>
				<view class="grace-boxes-text">卡包</view>
			</view>
		</view>
		<!-- 九宫格 end -->
		<!-- 轮播图 -->
		<graceSwiper swiperId="garce-swiper-1" :swiperHeight="290" :items="swiperItems"></graceSwiper>
		<!-- 品牌广告 strat -->
		<view class="grace-title grace-nowrap grace-space-between" style="margin-top:12px;">
			<view class="grace-h5 grace-blod">品牌推荐</view>
			<navigator class="grace-more-r">更多<text class="grace-iconfont icon-arrow-right"></text></navigator>
		</view>
		<scroll-view class="grace-scroll-x" scroll-x style="margin-top:10px;">
			<view class="grace-items"><image src="../../static/pinpai/1.png" mode="widthFix"></image></view>
			<view class="grace-items"><image src="../../static/pinpai/2.png" mode="widthFix"></image></view>
			<view class="grace-items"><image src="../../static/pinpai/3.png" mode="widthFix"></image></view>
			<view class="grace-items"><image src="../../static/pinpai/4.png" mode="widthFix"></image></view>
			<view class="grace-items"><image src="../../static/pinpai/5.png" mode="widthFix"></image></view>
		</scroll-view>
		<!-- 单图广告 -->
		<view class="index-banner">
			<image src="../../static/index-banner.png" mode="widthFix"></image>
		</view>
		<!-- 分类产品展示 图片等大 可以循环多个分类及分类对应的商品 strat -->
		<view class="grace-title grace-nowrap grace-space-between" style="margin-top:12px;">
			<view class="grace-h5 grace-blod">某个分类</view>
			<navigator class="grace-more-r">更多<text class="grace-iconfont icon-arrow-right"></text></navigator>
		</view>
		<view class="grace-imgitems">
			<navigator url="../product-info/product-info" class="grace-items">
				<image src="https://img.alicdn.com/bao/uploaded/i2/452325706/O1CN011s1OQAszoPWK8Rt_!!0-item_pic.jpg" mode="widthFix"></image>
				<view class="grace-imgitems-text">拉风大衣</view>
				<view class="grace-imgitems-more">
					￥19.99
					<view class="grace-imgitems-button">购买</view>
				</view>
			</navigator>
			<navigator url="../product-info/product-info" class="grace-items">
				<image src="https://img.alicdn.com/bao/uploaded/i1/2787417447/O1CN0124sly8iXb80L4OS_!!0-item_pic.jpg" mode="widthFix"></image>
				<view class="grace-imgitems-text">特价T恤</view>
				<view class="grace-imgitems-more">
					￥9.99
					<view class="grace-imgitems-button">购买</view>
				</view>
			</navigator>
			<navigator url="../product-info/product-info" class="grace-items">
				<image src="https://img.alicdn.com/bao/uploaded/i2/452325706/O1CN011s1OQAszoPWK8Rt_!!0-item_pic.jpg" mode="widthFix"></image>
				<view class="grace-imgitems-text">拉风大衣</view>
				<view class="grace-imgitems-more">
					￥19.99
					<view class="grace-imgitems-button">购买</view>
				</view>
			</navigator>
			<navigator url="../product-info/product-info" class="grace-items">
				<image src="https://img.alicdn.com/bao/uploaded/i1/2787417447/O1CN0124sly8iXb80L4OS_!!0-item_pic.jpg" mode="widthFix"></image>
				<view class="grace-imgitems-text">特价T恤</view>
				<view class="grace-imgitems-more">
					￥9.99
					<view class="grace-imgitems-button">购买</view>
				</view>
			</navigator>
		</view>
		<!-- 分类产品展示 end -->
		<!-- 猜你喜欢 strat -->
		<view class="grace-title grace-nowrap grace-space-between" style="margin-top:12px;">
			<view class="grace-h5 grace-blod">猜你喜欢</view>
		</view>
		<view class="grace-waterfall">
			<view class="list" v-for="(lists, index1) in productList" :key="index1">
				<navigator url="../product-info/product-info" class="items" v-for="(products, index2) in lists" :key="index2">
					<image :src="products.img" class="imgs" mode="widthFix"></image>
					<view class="title">{{products.title}}</view>
					<view class="price">
						{{products.price}}
						<view class="tips">{{products.tip}}</view>
					</view>
				</navigator>
			</view>
		</view>
		<graceLoading :loadingType="loadingType"></graceLoading>
	</view>
	<!-- 主体 end -->
</template>
<script>
var page = 1, _self;
var dataObj = require('../../data/data.js');
var products = dataObj.products;
import graceSwiper from "../../graceUI/components/graceSwiper.vue";
import graceLoading from "../../graceUI/components/graceLoading.vue";
export default {
	data() {
		return {
			// 轮播数据
			swiperItems : [
				{ imgUrl: 'https://img.alicdn.com/tps/i4/TB16pkzxFzqK1RjSZSgSuwpAVXa.jpg_1080x1800Q90s50.jpg', path : ""},
				{ imgUrl: 'https://aecpm.alicdn.com/simba/img/TB1W4nPJFXXXXbSXpXXSutbFXXX.jpg', path : ""},
				{ imgUrl: 'https://aecpm.alicdn.com/simba/img/TB1_JXrLVXXXXbZXVXXSutbFXXX.jpg', path : ""}
			],
			// 瀑布流加载
			loading: false,
			loadingType: 0,
			isEnd: false,
			productList : [[],[]],
			// 搜索
			searchKey:''
		}
	},
	onLoad() {
		_self = this;
		this.getList();
	},
	onReachBottom : function(){
		this.getList();
	},
	methods: {
		getList : function(){
			//最后一页判断[模拟，正式环境请根据 api 接口请求结果判断]
			if(page > 3){
				this.loadingType = 2;
				return;
			}
			this.loadingType = 1;
			//模拟api请求延迟关闭 Loading
			setTimeout(function () {
				var lArr = _self.productList[0];
				var rArr = _self.productList[1];
				//填充数组[此处的 products 数据应该来自与api接口数据]
				//数据格式见 "/data/data.js"
				products = dataObj.getArrRandomly(products); //打乱排序【模拟api】
				for (var i = 0; i < products.length; i++) {
					if (i % 2 == 0) {
						lArr.push(products[i]);
					} else {
						rArr.push(products[i]);
					}
				}
				_self.productList = [lArr, rArr];
				_self.loadingType = 0;
				page++;
			}, 1000);
		}
	},
	components:{
		graceSwiper,
		graceLoading
	}
}
</script>
<style>
.grace-search-in{border-radius:0;}
.input-placeholder{height:28upx !important; line-height:28upx ;}
.index-body{background:#E52852; height:350px; padding:8px 15upx; border-bottom-left-radius:30px; border-bottom-right-radius:30px;}
.grace-boxes-text{color:#FFF;}
.grace-scroll-x{background:#F2F3F4; padding:6px 5px !important; width:710upx !important;}
.grace-scroll-x image{width:100%;}
.grace-scroll-x .grace-items{width:230upx; height:auto; font-size:0; margin:0 6upx;}
.index-banner{margin:10px 0;}
.index-banner image{width:100%;}
</style>