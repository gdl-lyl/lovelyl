<template>
	<view class="content">
		<view class="page-body">
			<view class="page-section page-section-gap">
				<map style="width: 100%; height: 100%;" :controls="controls" :circles="circles" :polyline='polyline' :scale="scale"
				 :latitude="latitude" :longitude="longitude" :markers="covers">
				</map>
			</view>
		</view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}/16</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="line"></view>
		<view class="title">
			<image class="logo" src="/static/foot.jpg"></image>
			<view class="title-price">免费></view>
			<view class="title-one">泗州第一足球场</view>
			<view class="title-two">室外五人制{{number}}/18</view>
			<view class="title-time">12:00-14:00</view>
		</view>
		<view class="footer"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				number: '12',
				id:0, // 使用 marker点击事件 需要填写id
				tittle: 'map',
				latitude: 33.48289,
				longitude: 117.91106,
				covers: [{
					latitude: 33.48289, //纬度
					longitude: 117.91106, //经度
					iconPath: '/static/foot.jpg', //显示的图标			
					title: '阿打算', //标注点名
					label: { //为标记点旁边增加标签
						content: '足球场', //文本
						color: '#F76350', //文本颜色
						anchorX: 0, //label的坐标，原点是 marker 对应的经纬度
						anchorY: -80, //label的坐标，原点是 marker 对应的经纬度 
						// 					    x:39.909,//这个组件微信在1.2.0以后就废弃了
						// 					    y:116.39742,
						bgColor: '#fff', //背景色
						padding: 5, //文本边缘留白
						borderWidth: 1, //边框宽度
						borderColor: '#D84C29', //边框颜色							
						textAlign: 'right' //文本对齐方式。
					},
					callout: { //自定义标记点上方的气泡窗口 点击有效
						content: '地点1',
						color: '#F76350',
						fontSize: 12,
						borderRadius: 5,
					},
					// 					 anchor:{//经纬度在标注图标的锚点，默认底边中点
					// 						 x:5,
					// 						 y:1,
					// 					  }
				}, {
					latitude: 33.48289,
					longitude: 117.91106,
					iconPath: '/static/foot.jpg',
					title: '阿迪达斯',
					x: 33.48289,
					y: 117.91106,
					label: {
						content: '文本2',
						color: '#F76350',
						bgColor: '#fff',
						padding: 5,
						borderRadius: 4,
					},
					callout: {
						content: '地点2',
						color: '#F76350',
						fontSize: 12
					}
				}],
				scale: 15, //地图层级
				controls: [{ //在地图上显示控件，控件不随着地图移动
					id: 1, //控件id
					iconPath: '/static/foot.jpg', //显示的图标	
					position: { //控件在地图的位置
						left: 15,
						top: 15,
						width: 50,
						height: 50
					},
				}],
				// circles: [{ //在地图上显示圆
				// 	latitude: 33.411939,
				// 	longitude: 117.97575699999993,
				// 	fillColor: "#FFC41F", //填充颜色
				// 	color: "#12A1DD", //描边的颜色
				// 	radius: 400, //半径
				// 	strokeWidth: 2 //描边的宽度
				// }],
				polyline: [{ //指定一系列坐标点，从数组第一项连线至最后一项
					points: [{
							latitude: 33.48289,
							longitude: 117.91106
						},
						{
							latitude: 33.48289,
							longitude: 117.91106
						},
					],
					color: "#0000AA", //线的颜色
					width: 2, //线的宽度
					dottedLine: true, //是否虚线
					arrowLine: true, //带箭头的线 开发者工具暂不支持该属性
				}],


			};
		},
		onLoad() {
			uni.getLocation({ //获取当前的位置坐标
				type: 'wgs84',
				success: function(res) {
					console.log('当前位置的经度：' + res.longitude);
					console.log('当前位置的纬度：' + res.latitude);
				}
			});
			// 			uni.chooseLocation({
			// 				success: function (res) {
			// 					console.log('位置名称：' + res.name);
			// 					console.log('详细地址：' + res.address);
			// 					console.log('纬度：' + res.latitude);
			// 					console.log('经度：' + res.longitude);
			// 				}
			// 			});
			setTimeout(() => {
				this.$u.route({
					url: 'pages/wxCenter/wxCenter',
					params: {
						name: 'lisa'
					}
				})
			}, 2000)
		}
	}
</script>
<style>
	.content {
		height: 100px;

	}

	.title {
		width: 100%;
	}

	.logo {
		float: left;
		height: 64px;
		width: 64px;
		margin-left: 24px;
	}

	.title-price {
		float: right;
		margin-top: 24px;
		margin-right: 32px;
	}

	.title-one {
		margin-top: 16px;
		margin-left: 160px;
		font-size: 14px;
	}

	.title-two {
		margin-top: 8px;
		margin-left: 160px;
		font-size: 12px;
	}

	.title-time {
		margin-top: 8px;
		margin-left: 160px;
		font-size: 12px;
	}

	.line {
		background-color: #E5E5EA;
		height: 1px;
		margin-top: 8px;
		width: 90%;
		margin-left: 5%;
	}
	.footer{
		margin-bottom: 64px;
	}
</style>

