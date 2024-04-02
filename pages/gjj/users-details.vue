<template>
	<view class="main">
		<nav :style="{ height: $store.state.BH + 10 + 'px' }"></nav>
		<view class="top-nav">
			<image class="logo" src="/static/img/gjj-img/779.png" mode=""></image>
			<view class="jiaonang" :style="{ top: $store.state.BH + 20 + 'px' }" @click="GoHome">
				<image class="sc" src="/static/img/gjj-img/887.png" mode=""></image>
				<image class="jn" src="/static/img/gjj-img/46.png" mode=""></image>
			</view>
		</view>
		<view class="content-title">
				<view class="left">
					<view class="before"></view>
					<view class="title">个人信息</view>
				</view>
			</view>
	</view>

</template>

<script>
export default{
	methods:{
		GoHome() {
			uni.reLaunch({
				url: '/pages/index/index'
			});
		},
	}
}
</script>

<style lang="scss">
	.main {
		.top-nav {
			position: relative;
			padding: 15rpx 20rpx;
			.logo {
				width: 505rpx;
				height: 104rpx;
			}
			.jiaonang {
				position: fixed;
				right: 30rpx;
				top: 15rpx;
				.sc {
					width: 52rpx;
					height: 52rpx;
					margin-right: 15rpx;
				}
				.jn {
					width: 138rpx;
					height: 52rpx;
				}
			}
		}
	.content-title {
		padding: 0 67rpx 0 30rpx;
		padding-top: 32rpx;
		display: flex;
		justify-content: space-between;
		.left {
			display: flex;
			align-items: center;
			.before {
				margin-right: 20rpx;
				width: 8rpx;
				height: 28rpx;
				background: linear-gradient(180deg, #284cc7 0%, #3874f6 100%);
			}
			.title {
				font-size: 31rpx;
				font-weight: 800;
				color: #000000;
			}
		}
		.right {
			font-size: 28rpx;
			font-weight: 400;
			color: #153f9a;
			display: flex;
			align-items: center;
			image {
				width: 32rpx;
				height: 14rpx;
			}
		}
	}
	}
</style>