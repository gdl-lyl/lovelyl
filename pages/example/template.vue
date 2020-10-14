<template>
	<view>
		<view class="u-flex user-box u-p-l-30 u-p-r-20 u-p-b-30 u-p-t-30">
			<view class="u-m-r-10">
				<view class="u-demo-wrap">
					<view class="u-demo-area">
						<u-avatar 
							:mode="mode" 
							:size="size" 
							:src="src" 
							:text="text"
							:showLevel="showLevel"
							:showSex="showSex"
							:sexIcon="sexIcon"
							:bgColor='bgColor'
						></u-avatar>
					</view>
					
				</view>
			</view>
		</view>
		<view class="u-m-t-20">
		<u-grid :col="4" :border ="false">
			<u-grid-item>
				<u-icon name="photo" :size="46"></u-icon>
				<view class="grid-text">待付款</view>
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
		<view class="u-m-t-20">
			<u-cell-group>
				<u-cell-item icon="photo" title="收获地址"></u-cell-item>
				<u-cell-item icon="coupon" title="优惠券"></u-cell-item>
				<u-cell-item icon="heart" title="我的关注"></u-cell-item>
			</u-cell-group>
		</view>

		<view class="u-m-t-20">
			<u-cell-group>
				<u-cell-item icon="setting" title="配送时间"></u-cell-item>
				<u-cell-item icon="setting" title="在线客服"></u-cell-item>
				<u-cell-item icon="setting" title="帮助与反馈"></u-cell-item>
			</u-cell-group>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				show: true,
				mode: 'circle',
				src: 'http://pic2.sc.chinaz.com/Files/pic/pic9/202002/hpic2119_s.jpg',
				text: '', // 优先级比src高
				size: '90',
				showLevel: true,
				showSex: true,
				sexIcon: 'man',
				bgColor: '#fcbd71'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	page {
		background-color: #ededed;
	}

	.camera {
		width: 54px;
		height: 44px;

		&:active {
			background-color: #ededed;
		}
	}

	.user-box {
		background-color: #fff;
	}
</style>
