<template>
	<view>
		<view class="top"  ></view>
		
			<view class="daohang" >
				<image  src="../../static/shouye/xj.png" mode="aspectFit" @click="img()"></image>
				<scroll-view class="grace-tab-title" :scroll-x="true" :scroll-into-view="titleShowId">
					<view 
					v-for="(tab, index) in tabs" :class="[tabCurrentIndex == index ? 'grace-tab-current' : '']" 
					:id="'tabTag-'+index" 
					@tap="tabChange" 
					:key="index">{{tab.name}}</view>
				</scroll-view>
				
				<!-- 加号 -->
			  <view class="grace-bg-white grace-common-mt grace-padding grace-common-border">
			     <view style="min-height:30px; width:92%; margin:0 auto; position:relative;">
			        
			         <view class="demo-btn-1" id="demo-btn-1">
			             <image src="https://staticimgs.oss-cn-beijing.aliyuncs.com/popupmenu.png" mode="widthFix" @tap="showMenu1"></image>
			         </view>
			         <!-- gracePopupMenu 组件外层定位必须为 position:relative;  -->
			         <gracePopupMenu :show="menu1Show" :top="menu1Top" v-on:hideMenu="hideMenu">
			             <view class="grace-list" style="background:#4C4C4C; border:0;">
			                 <view class='items'>
			                     <view class="icons">
			                         <image src="../../static/wo/xiezuo.png" mode="widthFix"></image>
			                     </view>
			                     <navigator url="../write/write"><view class="title" @tap="tap1">写博客</view></navigator>
			                 </view>
			                 <view class='items'>
			                     <view class="icons">
			                         <image src="../../static/wo/jiu01.png"></image>
			                     </view>
			                     <view class="title"  @tap="tap2">图片</view>
			                 </view>
			                 <view class='items'>
			                     <view class="icons">
			                         <image src="../../static/wo/shipin.png" mode="widthFix"></image>
			                     </view>
			                     <view class="title" @tap="tap3">视频</view>
			                 </view>
			             </view>
			         </gracePopupMenu>
			     </view>
			 </view>
				<!-- 加号 -->
			</view>
		
			
			
			
			 <view style="height:100upx ;"></view> 
		<view class="neirong">
			<swiper class="grace-tab-swiper" :current="swiperCurrentIndex" @change="swiperChange" style="height:2000upx;">
				<!-- 第一页 -->
				<swiper-item class="demo-img">
					<view class="grace-news-list">
                <navigator url="../info/info">
                    <view class="grace-news-list-items">
                      <view class="grace-news-list-title">
                            <view class="grace-news-list-title-main">三问奔驰维权事件：服务费进了谁腰包？能否三倍赔偿？</view>
                            <text class="grace-news-list-title-desc grace-text-overflow">据女车主哭诉，她购买了一辆66万元的奔驰车作为自己30岁的生日礼物。</text>
							<image src="../../static/shouye/diyixw.jpg" class="grace-news-list-img grace-list-imgs-l" mode="widthFix"></image>
							<image src="../../static/shouye/dierxw-2.jpg" class="grace-news-list-img grace-list-imgs-l" mode="widthFix"></image>
                        </view>
                    </view>
                </navigator>
                <navigator>
                    <view class="grace-news-list-items">
                        <view class="grace-news-list-title">
                            <view class="grace-news-list-title-main">习近平强调的制度创新 海南自贸区一年交出亮眼成绩单</view>
                            <text class="grace-news-list-title-desc grace-text-overflow">在总书记讲话精神的指引下，一年间海南省推出一系列重要举措，优化营商环境、支持人才引进、加强科技创新，坚持以制度创新为抓手，推动海南自贸区高标准、高质量建设，涌现出许多有亮点有特色的典型案例，央视网带您一图了解！

</text>
                        </view>
                        <image src="../../static/shouye/dier0201.jpg" class="grace-news-list-img grace-list-imgs-r" mode="widthFix"></image>
                        <view class="grace-news-tips grace-news-tips-r">新闻</view>
                    </view>
                </navigator>
                <navigator>
                    <view class="grace-news-list-items">
                        <image src="../../static/shouye/di0202.jpg" class="grace-news-list-img grace-list-imgs-l" mode="widthFix"></image>
                        <view class="grace-news-list-title">
                            <view class="grace-news-list-title-main">？歌手刘欢突发心脏病，这个关键动作救回自己一命！1分钟变化竟如此凶险……收藏！</view>
                            <text class="grace-news-list-title-desc grace-text-overflow">刘欢可以说是一位非常有实力歌手和音乐人，演唱了《心中的太阳》《好汉歌》《千万次的问》《弯弯的月亮》等多个脍炙人口的歌曲，深受很多人喜欢。不过近日。</text>
                        </view>
                    </view>
                    <view class="grace-news-list-info">发布于2天前    xx次浏览<text>其他元素</text></view>
                </navigator>
                <navigator>
                    <view class="grace-news-list-img-news">
                        <view class="grace-news-list-title-main">新发现!NASA宇航员太空待340天 DNA发生永久突变</view>
                        <view class="grace-news-list-imgs">
                            <image src="../../static/shouye/di0301.jpg" mode="widthFix"></image>
                            <image src="../../static/shouye/di0302.png" mode="widthFix"></image>
                            <image src="../../static/shouye/di0303.jpg" mode="widthFix"></image>
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
                    <view class="grace-news-list-img-news">
                        <view class="grace-news-list-title-main">澳总理用汉语“你好”跟韩国人打招呼 有人不高兴了……</view>
                        <view class="grace-news-list-img-big"><image src="../../static/shouye/di0401.jpg" mode="widthFix"></image></view>
                    </view>
                    <view class="grace-news-list-info">发布于2天前    xx次浏览<text>其他元素</text></view>
                </navigator>
            </view>
				</swiper-item>
				
				
				<!-- d第二页 -->
				<swiper-item class="demo-img">
					<view class="grace-news-list">
					<navigator>
					    <view class="grace-news-list-img-news">
					        <view class="grace-news-list-title-main">新发现!NASA宇航员太空待340天 DNA发生永久突变</view>
					        <view class="grace-news-list-imgs">
					            <image src="../../static/shouye/di0301.jpg" mode="widthFix"></image>
					            <image src="../../static/shouye/di0302.png" mode="widthFix"></image>
					            <image src="../../static/shouye/di0303.jpg" mode="widthFix"></image>
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
					    <view class="grace-news-list-img-news">
					        <view class="grace-news-list-title-main">澳总理用汉语“你好”跟韩国人打招呼 有人不高兴了……</view>
					        <view class="grace-news-list-img-big"><image src="../../static/shouye/di0401.jpg" mode="widthFix"></image></view>
					    </view>
					    <view class="grace-news-list-info">发布于2天前    xx次浏览<text>其他元素</text></view>
					</navigator>
					</view>
				</swiper-item>
				
			</swiper>
		</view>
		
        
		
	</view>
</template>

<script>
	import gracePopupMenu from '../../graceUI/components/gracePopupMenu.vue';
	export default {
		data() {
			return {
				
				  menu1Show : false,
				menu1Top  : 30,
				
				tabCurrentIndex: 0,
				swiperCurrentIndex: 0,
				tabs: [
					{ name: '关注', id: 'guanzhu' },
					{ name: '推荐', id: 'tuijian' },
					
				],
				titleShowId : 'tabTag-0'
				
			}
		},
		onLoad() {

		},
		methods: {
			img:function(){
				uni.chooseImage({
					count:3,
					sizeType:"compressed",
					success() {
						console.log(res);
					}				})
			},
			
			tabChange: function (e) {
				var index = e.target.id.replace('tabTag-', '');
				this.swiperCurrentIndex = index;
				this.tabCurrentIndex    = index;
				this.titleShowId        = 'tabTag-'+index;
			},
			swiperChange: function (e) {
				var index = e.detail.current;
				this.tabCurrentIndex = index;
				this.titleShowId        = 'tabTag-'+index;
			},
			
			showMenu1 : function(e){
			        if(this.menu1Show){
			            this.menu1Show = false;
			            return ;
			        }
			        // 动态调整菜单的 top 值
			        // 原理 : 获取按钮的高度 = 菜单的 top 值
			        let view = uni.createSelectorQuery().select("#demo-btn-1");
			        view.fields({size: true}, data => {
			          this.menu1Show = true;
			          this.menu1Top = data.height;
			        }).exec();
			    },
			    // 关闭菜单方法
			    hideMenu : function(){
			        this.menu1Show = false;
			    },
			    // 菜单点击函数
			    tap1 : function(){
// // 			        uni.showToast({
// // 			            // title:"您点击了第1个菜单",
// 			            icon: "none"
// 			        });
			        this.hideMenu();
			    },
			    tap2 : function(){
// 			        uni.showToast({
// 			            title:"您点击了第2个菜单",
// 			            icon: "none"
// 			        });
			        this.hideMenu();
			    },
			    tap3 : function(){
// 			        uni.showToast({
// 			            title:"您点击了第3个菜单",
// 			            icon: "none"
// 			        });
			        this.hideMenu();
			    }
			},
			components:{
			    gracePopupMenu
			}

		}

</script>

<style>
	
	 .daohang{  width: 100%;  
    position: fixed;  
    /* background-color: #F8F8F8; */  
    top: 0;  
    z-index: 999; 
	
	} 
	.daohang{height:100upx; width: 100%;  display: flex; justify-content: space-between; align-items: center;}
	.daohang image{ height: 60upx; }
	
	/* 页面个性化样式 */
	.demo-btn-1{width:28px; height:28px; float:right; border-radius:3px; border:1px solid #00C777; text-align:center; font-size:0;}
	.demo-btn-1 image{width:18px; height:18px; margin:5px;}
	.grace-list view{color:#FFF;}
	.grace-list .title{border:0;}
</style>
