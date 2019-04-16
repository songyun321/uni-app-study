<template>
    <view>
        <scroll-view class="grace-tab-title grace-center" scroll-x="true" id="grace-tab-title">
            <view v-for="(tab, index) in tabs" :key="index" :class="[tabCurrentIndex == index ? 'grace-tab-current' : '']" :id="'tabTag-'+index" @tap="tabChange">{{tab.name}}</view>
        </scroll-view>
        <swiper class="grace-tab-swiper-full" :current="swiperCurrentIndex" @change="swiperChange" :style="{height:tabHeight+'px'}">
            <!-- 循环新闻项目 -->
            <swiper-item >
				<!-- 内容 -->
				
				<view class="grace-card-view">
					<text class="wenzi">uni-app终极跨平台解决方案</text>
				    <view class="body">
						<video src="https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4 " controls></video>
				        <view class="img" style="width: 10upx;"></view>
				        
				    </view>
				    <view class="footer">
				        <view >转发</view>
				        <view>评论</view>
				        <view >点赞</view>
				    </view>
					
					<view class="grace-card-view">
						<text class="wenzi">uni-app终极跨平台解决方案</text>
					    <view class="body">
							<video src="https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4 " controls></video>
					        <view class="img" style="width: 10upx;"></view>
					        
					    </view>
					    <view class="footer">
					        <view >转发</view>
					        <view>评论</view>
					        <view >点赞</view>
					    </view>
				
				
               <!-- 内容 -->
            </swiper-item>
			
			<swiper-item >
				<!-- 内容 -->
				
				
				<view class="grace-card-view">
					<text class="wenzi">uni-app终极跨平台解决方案</text>
				    <view class="body">
						<video src="https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4 " controls></video>
				        <view class="img" style="width: 10upx;"></view>
				        
				    </view>
				    <view class="footer">
				        <view >转发</view>
				        <view>评论</view>
				        <view >点赞</view>
				    </view>
				
			   <!-- 内容 -->
			</swiper-item>
			
			<swiper-item >
				<!-- 内容 -->
				
				
				<view class="grace-card-view">
					<text class="wenzi">uni-app终极跨平台解决方案</text>
				    <view class="body">
						<video src="https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4 " controls></video>
				        <view class="img" style="width: 10upx;"></view>
				        
				    </view>
				    <view class="footer">
				        <view >转发</view>
				        <view>评论</view>
				        <view >点赞</view>
				    </view>
				
			   <!-- 内容 -->
			</swiper-item>
			
			<swiper-item >
				<!-- 内容 -->
				
				<view class="grace-card-view">
					<text class="wenzi">uni-app终极跨平台解决方案</text>
				    <view class="body">
						<video src="https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4 " controls></video>
				        <view class="img" style="width: 10upx;"></view>
				        
				    </view>
				    <view class="footer">
				        <view >转发</view>
				        <view>评论</view>
				        <view >点赞</view>
				    </view>
				
			   <!-- 内容 -->
			</swiper-item>
        </swiper>
    </view>
</template>
<script>
var _self;
//默认新闻数据（来自api请求）
//每个选项下面的新闻列表
var news = [
  
];
//对应下面3个标签的新闻内容数据
var newsAll = [news, news, news];
import graceLoading from "../../graceUI/components/graceLoading.vue"
export default {
    data() {
        return {
            tabCurrentIndex: 0,
            swiperCurrentIndex: 0,
            tabHeight : 300,
            tabs: [
                //标签名称 , 分类 id , 加载更多, 加载的页码
                { name: '日榜', id: 'guanzhu' , loadingType : 0, page : 1},
                { name: '推荐', id: 'tuijian', loadingType: 0, page: 1},
                { name: '故事', id: 'tiyu', loadingType: 0, page: 1},
				{ name: '明星', id: 'mingxing', loadingType: 0, page: 1}
            ],
            newsAll: newsAll
        }
    },
    onLoad:function(){
        _self = this;
    },
    onReady: function () {
        //获取屏幕高度及比例
        var winInfo = uni.getSystemInfo({
            success: function (res) {
                var windowHeight = res.windowHeight;
                //获取头部标题高度
                var dom = uni.createSelectorQuery().select('#grace-tab-title')
                dom.fields({size: true}, res2 => {
                    if(!res2){return ;}
                    //计算得出滚动区域的高度
                    _self.tabHeight = windowHeight - res2.height;
                }).exec();
            }
        });
    },
    methods:{
        tabChange: function (e) {
            var index = e.target.id.replace('tabTag-', '');
            this.swiperCurrentIndex = index;
            this.tabCurrentIndex    = index;
        },
        swiperChange: function(e){
            var index = e.detail.current;
            this.tabCurrentIndex = index;
        },
        //每个选项滚动到底部
        scrollend:function(e){
            //获取是哪个选项滚动到底？
            var index = e.currentTarget.dataset.scindex;
            console.log(index);
            //可以利用 tabs 携带的分类id 与服务器交互请求对应分类的数据
            console.log(this.tabs[index].id);
            //加载更多的演示
            //判断当前是否正在加载
            if (this.tabs[index].loadingType === 1){
                return false;
            }
            //判断是否是最后一页
            console.log(this.tabs[index].page)
            if (this.tabs[index].page > 3){
                this.tabs[index].loadingType = 2;//全部
                return ;
            }
            this.tabs[index].loadingType = 1;//加载中
            //模拟延迟
            setTimeout(function(){
                _self.newsAll[index] = _self.newsAll[index].concat(news);
                //分页
                _self.tabs[index].page++;
                _self.tabs[index].loadingType = 0;//恢复加载状态
                //
            }, 1000);
        }
    },
    components:{
        graceLoading
    }
}
</script>
<style>
page{background:#FFFFFF;}

.wenzi{font-size: 50upx; color: #007AFF;}
</style>