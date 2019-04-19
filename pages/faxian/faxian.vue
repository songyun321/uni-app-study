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
		<!-- 热搜条 -->
		<view class="resou">
			<view class="resouzi"> <image src="../../static/faxian/search.png" mode="aspectFit"></image>热搜</view>
			<view class="neinong">
				<!-- 左侧 -->
				<view class="zuoce">
					<view style="border-bottom-width: 30upx;">毕福剑<image src="../../static/faxian/bao.png" mode=""></image></view>
					<view style="border-bottom-width: 30upx;">王牌对王牌收官之战<image src="../../static/faxian/jian.png" mode=""></image></view>
					<view style="border-bottom-width: 30upx;">长期睡眠不足..<image src="../../static/faxian/re.png" mode=""></image></view>
					<view style="border-bottom-width: 30upx;">韩国富二代<image src="../../static/faxian/xin.png" mode=""></image></view>
					
				</view>
				<!-- 左侧 -->
				<!-- 右侧 -->
				<view class="youce">
					<view style="border-bottom-width: 30upx;">中戏<image src="../../static/faxian/jian.png" mode=""></image></view>
					<view style="border-bottom-width: 30upx;">giaogiaogiao <image src="../../static/faxian/re.png" mode=""></image></view>
					<view style="border-bottom-width: 30upx;">吴亦凡 大碗面<image src="../../static/faxian/xin.png" mode=""></image></view>
					<view style="border-bottom-width: 30upx; color:	#FFA500 ;">更多热搜 > </view>
					
					
				</view>
				<!-- 右侧 -->
			</view>
		</view>
		<!-- 热搜条 -->
		<view style="height: 20upx; background-color: 	#A9A9A9;"></view>
		<!-- 轮播 -->
		 
        <view class="grace-bg-white grace-common-mt grace-common-border">
            <!-- swiper 的高度 = (外层宽度 720upx ) * (图片的 宽高比例 图片高度/ 图片宽度) -->
            <!-- 本例 图片宽度 : 990px 高度 : 400px -->
            <!-- 计算得出 swiper 的高度 = 720 * 400 / 990 = 290upx-->
           
           
            <swiper class="grace-swiper" autoplay="true" indicator-color="rgba(255, 255, 255, 1)" indicator-active-color="#00B26A" style="height:290upx" interval="5000">
                <swiper-item >
                    <navigator url='item.path' >
                        <image src='../../static/faxian/giao04.jpg' mode='widthFix'></image>
                        <view class="title">giao哥同款营养品</view>
                    </navigator>
                </swiper-item>
				
				<swiper-item >
				    <navigator url='item.path' >
				        <image src='../../static/faxian/giao05.jpg' mode='widthFix'></image>
				        <view class="title">giao哥参加中国新说唱</view>
				    </navigator>
				</swiper-item>
				
				<swiper-item >
				    <navigator url='item.path' >
				        <image src='../../static/faxian/giaogiaogiaogiaogiao03.jpg' mode='widthFix'></image>
				        <view class="title">隔壁小阿giao</view>
				    </navigator>
				</swiper-item>
            </swiper>
        </view>
		<!-- 轮播 -->
		
		<!-- 选项卡 -->
		<view class="grace-tab" style="margin-top:30px;">
                <scroll-view class="grace-tab-title" scroll-x="true">
                    <view v-for="(tab, index) in tabs" :class="[tabCurrentIndex == index ? 'grace-tab-current' : '']"  :id="'tabTag-'+index" @tap="tabChange" :key="index">{{tab.name}}</view>
                </scroll-view>
                <swiper class="grace-tab-swiper" :current="swiperCurrentIndex" @change="swiperChange" style="height:850upx;">
                    <swiper-item>
			<view class="grace-news-list">
				
				
			    <navigator>
                    <view class="grace-news-list-img-news">
                        <view class="grace-news-list-title-main">giaogiaogiaogiaogiao</view>
                        <view class="grace-news-list-imgs">
                            <image src="../../static/faxian/giaogiao01.jpg" mode="widthFix"></image>
                            <image src="../../static/faxian/giaogiao02.jpg" mode="widthFix"></image>
                            <image src="../../static/faxian/giaogiao03.jpg" mode="widthFix"></image>
                        </view>
                    </view>
                    <view class="grace-news-list-info">
                        <view>
                            <text class="grace-iconfont icon-time2"></text>2天前
                            <text class="grace-iconfont icon-eye" style="margin-left:20px;"></text>99次浏览
                        </view>
                    </view>
                </navigator>
				
				<navigator>
                    <view class="grace-news-list-items">
                        <view class="grace-news-list-title">
                            <view class="grace-news-list-title-main">giaogiaogiaogiaogiaogiaogiaogiaogiaog</view>
                            <text class="grace-news-list-title-desc grace-text-overflow">giaogiaogiaogiaogiaogiaogiaogiaogiaog</text>
                        </view>
                        <image src="../../static/faxian/giaogiao04.jpg" class="grace-news-list-img grace-list-imgs-r" mode="widthFix"></image>
                        <view class="grace-news-tips grace-news-tips-r">giao</view>
                    </view>
                </navigator>
				
				
				  <navigator>
                    <view class="grace-news-list-items">
                        <image src="../../static/faxian/giaogiao05.jpg" mode="widthFix"></image>
                        <view class="grace-news-list-title">
                            <view class="grace-news-list-title-main">giaogiaogiaogiaogiaogiaogiaogiaogiaog</view>
                            <text class="grace-news-list-title-desc grace-text-overflow">giaogiaogiaogiaogiaogiao</text>
                        </view>
                    </view>
                </navigator>
				
				
				
				
				
			</view>
					</swiper-item>
                    <swiper-item>
						
						<view class="grace-news-list">
							
							
						    <navigator>
						        <view class="grace-news-list-img-news">
						            <view class="grace-news-list-title-main">yaoyaoyaoyao</view>
						            <view class="grace-news-list-imgs">
						                <image src="../../static/faxian/yaoyao01.jpg" mode="widthFix"></image>
						                <image src="../../static/faxian/yaoyao02.jpg" mode="widthFix"></image>
						                <image src="../../static/faxian/yaoyao03.jpg" mode="widthFix"></image>
						            </view>
						        </view>
						        <view class="grace-news-list-info">
						            <view>
						                <text class="grace-iconfont icon-time2"></text>2天前
						                <text class="grace-iconfont icon-eye" style="margin-left:20px;"></text>99次浏览
						            </view>
						        </view>
						    </navigator>
							
							<navigator>
						        <view class="grace-news-list-items">
						            <view class="grace-news-list-title">
						                <view class="grace-news-list-title-main">yaoyaoyaoyao</view>
						                <text class="grace-news-list-title-desc grace-text-overflow">yaoyaoyaoyaoyaoyaoyaoyao</text>
						            </view>
						            <image src="../../static/faxian/yaoyao05.jpg" class="grace-news-list-img grace-list-imgs-r" mode="widthFix"></image>
						            <view class="grace-news-tips grace-news-tips-r">yao</view>
						        </view>
						    </navigator>
							
							
							  <navigator>
						        <view class="grace-news-list-items">
						            <image src="../../static/faxian/yaoyao06.jpg" mode="widthFix"></image>
						            <view class="grace-news-list-title">
						                <view class="grace-news-list-title-main">yaoyaoyaoyaoyaoyaoyaoyao</view>
						                <text class="grace-news-list-title-desc grace-text-overflow">yaoyaoyaoyao</text>
						            </view>
						        </view>
						    </navigator>
							
							
							
							
							
						</view>
					</swiper-item>
                    <swiper-item>didididididiiddidiidididdiiddiiddi</swiper-item>
                    
                </swiper>
            </view>
		<!-- 选项卡 -->
		
		
	</view>
</template>

<script>
	var _self;
	export default {
		data() {
			return {
				 swiperItems : [],
				 
				  tabCurrentIndex: 0,
            swiperCurrentIndex: 0,
            tabs: [
                { name: '热门话题', id: 'guanzhu' },
                { name: '话题榜', id: 'tuijian' },
                { name: '超话社区', id: 'tiyu' },
                
            ]
			};
		},
	 methods:{
        tabChange: function (e) {
            var index = e.target.id.replace('tabTag-', '');
            this.swiperCurrentIndex = index;
            this.tabCurrentIndex    = index;
        },
        swiperChange: function (e) {
            var index = e.detail.current;
            this.tabCurrentIndex = index;
        }
    }
		
		
	}
</script>

<style>
.resou{ height: 230upx;margin-left: 20upx;}
.resouzi{ height: 40upx; display: flex;flex-wrap: nowrap;font-size: small;border-bottom-width: 30upx;}
.resouzi image{height: 30upx;width: 30upx;}
.neinong{border-width: 20upx;}
.zuoce{width: 350upx;float: left;border-left-width: 20upx;}
.zuoce image{height: 30upx;width: 30upx;}

.youce{width: 350upx;float: right;border-left-width: 20upx; }
.youce image{height: 30upx;width: 30upx;}
</style>
