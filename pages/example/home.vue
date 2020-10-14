<template>
	<view class="wrap">
		<view class="u-demo-wrap">
			<view>
				<u-search v-model="value" @change="change2" @custom="custom" @search="search" :shape="shape" :clearabled="clearabled"
				 :show-action="showAction" :input-align="inputAlign" @clear="clear"></u-search>
			</view>
			<view class="u-demo-area">
				<u-tabs v-if="control" bg-color="#fafafa" :bold="bold" :active-color="activeColor" :list="list" @change="change"
				 :current="current" :is-scroll="isScroll"></u-tabs>
			</view>
		<view>
			<u-swiper @change="change1" :height="250" :list="list" :title="title" :effect3d="effect3d" 
			:indicator-pos="indicatorPos" :mode="mode" :interval="3000" @click="click"></u-swiper>
		</view>
		<view class="u-m-t-20">
		<u-grid :col="5" :border ="false">
			<u-grid-item>
				<u-icon name="photo" :size="46"></u-icon>
				<view class="grid-text">水果</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="lock" :size="46"></u-icon>
				<view class="grid-text">蔬菜</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="hourglass" :size="46"></u-icon>
				<view class="grid-text">肉禽蛋品</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="shopping-cart" :size="46"></u-icon>
				<view class="grid-text">海鲜水产</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="photo" :size="46"></u-icon>
				<view class="grid-text">粮油调味</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="lock" :size="46"></u-icon>
				<view class="grid-text">熟食卤味</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="hourglass" :size="46"></u-icon>
				<view class="grid-text">待评价</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="shopping-cart" :size="46"></u-icon>
				<view class="grid-text">全部订单</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="lock" :size="46"></u-icon>
				<view class="grid-text">待收货</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="hourglass" :size="46"></u-icon>
				<view class="grid-text">待评价</view>
			</u-grid-item>
			<u-grid-item>
				<u-icon name="shopping-cart" :size="46"></u-icon>
				<view class="grid-text">全部订单</view>
			</u-grid-item>
		</u-grid>
		</view>
		</view>
	</view>
</template>

<script>
	import list from "./js.config.js";
	export default {
		data() {
			return {
				data: [{
					name: '关注'
				}, {
					name: '推荐'
				}, {
					name: '电影'
				}, {
					name: '电视剧'
				}, {
					name: '小视频'
				}, {
					name: '游戏'
				}, {
					name: '校园'
				}, {
					name: '影视'
				}, {
					name: '音乐'
				}],
				current: 0,
				sectionCurrent: 0,
				isScroll: true,
				tabCountIndex: 0,
				activeColor: this.$u.color['primary'],
				bold: true,
				control: true
			}
		},
		onLoad() {
			this.list = this.data;
		},
		methods: {
			change(index) {
				this.current = index;
			},
			change1(index) {
				// console.log(index);
			}
			
		}
	}
</script>

<style>
</style>

<style lang="scss" scoped>
	.u-cell-icon {
		width: 36rpx;
		height: 36rpx;
		margin-right: 8rpx;
	}
</style>
