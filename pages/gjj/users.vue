<template>
	<view class="main">
		<nav :style="{ height: $store.state.BH + 10 + 'px' ,backgroundColor:'#3874f6'}"></nav>
		<view class="top-nav">
			<view class="title">
				<image class="title-img" src="/static/bba.png" mode="" @click="back"></image>
				<text class="title-text">住房公积金账户</text>
			</view>
			<!-- <image class="logo" src="/static/img/gjj-img/779.png" mode=""></image> -->
			<view class="jiaonang" :style="{ top: $store.state.BH + 20 + 'px' }" @click="GoHome">
				<image class="sc" src="/static/img/gjj-img/887.png" mode=""></image>
				<image class="jn" src="/static/img/gjj-img/46.png" mode=""></image>
			</view>

		</view>
		<view class="card">
			<!-- 				<view class="content-title">
				<view class="left">
					<view class="before"></view>
					<view class="title">个人信息</view>
				</view>
				</view>
				<view class="line">
					<u-line />
				</view> -->
			<view class="info">
				<view class="item">
					<text class="label">个人账户状态</text>
					<text class="value">正常缴存</text>
				</view>
				<view class="item">
					<text class="label">个人账户余额</text>
					<text class="value">18994.11</text>
				</view>
				<view class="item">
					<text class="label">个人账号</text>
					<text class="value">1028376472623212</text>
				</view>
				<view class="item">
					<text class="label">中心编号</text>
					<text class="value">10238712731231231</text>
				</view>
				<view class="item">
					<text class="label">中心名称</text>
					<text class="value">上海住房公积金管理中心</text>
				</view>
				<view class="details" @click="goDetails">
					<text>点击查看详情</text>
				</view>
			</view>

		</view>
		<!-- 	<view class="card">
			<view class="content-title">
			<view class="left">
				<view class="before"></view>
				<view class="title">中心信息</view>
			</view>
			</view>
			<view class="line">
				<u-line />
			</view>
			<view class="info">
				<view class="item">
					<text class="label">中心编号</text>
					<text class="value">3301000000000000</text>
				</view>
				<view class="item">
					<text class="label">中心名称</text>
					<text class="value">上海住房公积金管理中心</text>
				</view>
				<view class="item">
					<text class="label">单位名称</text>
					<text class="value">智联朝朝</text>
				</view>
				<view class="item">
					<text class="label">单位账号</text>
					<text class="value">102387281231</text>
				</view>
			</view>
	
	</view>
	<view class="card">
			<view class="content-title">
			<view class="left">
				<view class="before"></view>
				<view class="title">账户信息</view>
			</view>
			</view>
			<view class="line">
				<u-line />
			</view>
			<view class="info">
				<view class="item">
					<text class="label">个人缴存比例</text>
					<text class="value">12%</text>
				</view>
				<view class="item">
					<text class="label">单位缴存比例</text>
					<text class="value">12%</text>
				</view>
				<view class="item">
					<text class="label">个人缴存基数</text>
					<text class="value">9000.00</text>
				</view>
				<view class="item">
					<text class="label">个人月缴存额</text>
					<text class="value">1080.00</text>
				</view>
				<view class="item">
					<text class="label">单位月缴存额</text>
					<text class="value">1080.00</text>
				</view>
			</view>
	
	</view>
	 -->
	</view>

</template>

<script>
	export default {
		methods: {
			goDetails() {
				uni.navigateTo({
					url: '/pages/gjj/users-details'
				});
			},
			GoHome() {
				uni.reLaunch({
					url: '/pages/index/index'
				});
			},
			back(){
				uni.navigateBack();
			}
		}
	}
</script>

<style lang="scss">
	.main {
		$textColor: #A2A2A2;
		height: 100vh;
		background: #F6F6F6;

		.card {
			padding-top: 16rpx;
			background-color: #fff;
			margin-bottom: 40rpx;
		}

		.info {
			display: flex;
			flex-direction: column;
			padding: 0rpx 40rpx;
			padding-bottom: 40rpx;

			.item {
				display: flex;
				padding: 14rpx 0rpx;

				// justify-content: space-around;
				.label {
					color: $textColor;
					width: 200rpx;
				}

				.value {
					color: #595959;
					font-weight: 500;
					flex: 1;
					text-align: right;
				}
			}
		}

		.top-nav {
			position: relative;
			padding: 15rpx 20rpx;
			background-color: #3874f6;

			.title {
				width: 505rpx;
				height: 80rpx;
				display: flex;

				.title-text {
					font-size: 33rpx;
					color: #fff;
					font-weight: 600;
					letter-spacing: 2rpx;
				}

				.title-img {
					width: 40rpx;
					height: 40rpx;
					margin-right: 20rpx;
				}
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
					font-size: 30rpx;
					font-weight: 600;
					color: #5369BA;
					letter-spacing: 2rpx;
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

		.line {
			width: 94%;
			margin: 0 auto;
			padding-top: 20rpx;
			padding-bottom: 20rpx;
		}

		.details {
			display: flex;
			align-items: center;
			justify-content: end;
			font-size: 28rpx;
			margin-top: 20rpx;
			color: #476FD7;
			position: relative;
			margin-right: 20rpx;
			&:after {
				content: '';
				position: absolute;
				top: -50%rpx;
				right: -20rpx;
				width: 12rpx;
				height: 12rpx;
				border-top: 4rpx solid #476FD7;
				border-right: 4rpx solid #476FD7;
				transform: rotate(45deg);
			}
		}
	}
</style>