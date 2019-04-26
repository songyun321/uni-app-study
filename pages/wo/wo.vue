<template>
	<view>
		<!-- 头部 -->
		 <view class="grace-card-view">
            <view class="body">
                <view class="img"><image src="../../static/wo/touxmao.jpg" /></view>
                <view class="desc">
                    <view class="title">王大陆<text>补充信息</text></view>
                    
                    <view class="text">简介:  <text>好好学习天天向上</text></view>
                </view>
            </view>
            <view class="footer">
                <view class="grace-iconfont icon-home">博客</view>
                <view class="grace-iconfont icon-safe">关注</view>
                <view class="grace-iconfont icon-share">粉丝</view>
            </view>
        </view>
		<!-- <头部 -->
	<!-- 九宫格 -->
    <view class="grace-padding">
       
        <view class="grace-padding grace-bg-white grace-common-mt grace-common-border">
            <view style="padding:50upx 0;" class="grace-wrap">
               <navigator class="grace-boxes" url="../xiancecece/xiancecece">
                   <view class="grace-boxes-img">
                   <image src="../../static/wo/jiu01.png" mode="widthFix"></image>
                   </view>
                   <view class="grace-boxes-text">相册</view>
               </navigator>
                <navigator class="grace-boxes" url="../wodegus/wodegus">
                    <view class="grace-boxes-img">
                    <image src="../../static/wo/jiu02.png" mode="widthFix"></image>
                    </view>
                    <view class="grace-boxes-text">故事</view>
                </navigator>
               <navigator class="grace-boxes">
                   <view class="grace-boxes-img">
                   <image src="../../static/wo/jiu03.png" mode="widthFix"></image>
                   </view>
                   <view class="grace-boxes-text">我的赞</view>
               </navigator>
			   
                <navigator class="grace-boxes">
                    <view class="grace-boxes-img">
                    <image src="../../static/wo/jiu04.png" mode="widthFix"></image>
                    </view>
                    <view class="grace-boxes-text">粉丝服务</view>
                </navigator>
				
				
				<navigator class="grace-boxes" url="../qianbao/qianbao">
				    <view class="grace-boxes-img">
				    <image src="../../static/wo/jiu05.png" mode="widthFix"></image>
				    </view>
				    <view class="grace-boxes-text">钱包</view>
				</navigator>
				
				
				<navigator class="grace-boxes" url="../youyouyoux/youyouyoux">
				    <view class="grace-boxes-img">
				    <image src="../../static/wo/jiu06.png" mode="widthFix"></image>
				    </view>
				    <view class="grace-boxes-text">优选</view>
				</navigator>
				<navigator class="grace-boxes">
				    <view class="grace-boxes-img">
				    <image src="../../static/wo/jiu07.png" mode="widthFix"></image>
				    </view>
				    <view class="grace-boxes-text">头条</view>
				</navigator>
				<navigator class="grace-boxes">
				    <view class="grace-boxes-img">
				    <image src="../../static/wo/jiu08.png" mode="widthFix"></image>
				    </view>
				    <view class="grace-boxes-text">客服</view>
				</navigator>
                
            </view>
        </view>
    </view>
	<!-- 九宫格 -->
	<!-- 列表 -->
	<view class="grace-bg-white grace-common-mt">
            <view class="grace-list">
                <navigator class='items'>
                  <view class='items'>
                      <view class="icons">
                          <image src="../../static/wo/liebiao01.png" mode="widthFix"></image>
                      </view>
                      <view class="title">收藏<text></text></view>
                      <view class="arrow-right"></view>
                  </view>
               </navigator>
				
                <navigator class='items'>
                   <view class='items'>
                       <view class="icons">
                           <image src="../../static/wo/lieb04%20(5).png" mode="widthFix"></image>
                       </view>
                       <view class="title">相册<text></text></view>
                       <view class="arrow-right"></view>
                   </view>
                </navigator>
				
                <navigator class='items'>
                  <view class='items'>
                      <view class="icons">
                          <image src="../../static/wo/liebiao03.png" mode="widthFix"></image>
                      </view>
                      <view class="title">卡包<text></text></view>
                      <view class="arrow-right"></view>
                  </view>
               </navigator>
			   
                <navigator class='items'>
                  <view class='items'>
                      <view class="icons">
                          <image src="../../static/wo/lieb04%20(1).png" mode="widthFix"></image>
                      </view>
                      <view class="title">表情<text></text></view>
                      <view class="arrow-right"></view>
                  </view>
               </navigator>
			   
                 <navigator class='items' url="../shezhi/shezhi">
                   <view class='items'>
                       <view class="icons">
                           <image src="../../static/wo/liebiao05.png" mode="widthFix"></image>
                       </view>
                       <view class="title">设置<text></text></view>
                       <view class="arrow-right"></view>
                   </view>
                </navigator>
                    <view class="arrow-right"></view>
                </view>
            </view>
        </view>
	
		<!-- 列表 -->
	
	</view>
</template>
<script>
export default{
    data() {
        return {
            staticUrl: this.staticUrl
        }
    }
}
</script>
<style>

.grace-boxes-img image{width:80upx; height:80upx; border-radius:8rpx;}

</style>