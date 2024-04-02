<template>
	<view class="main">
		<nav :style="{ height: $store.state.BH + 'px' }"></nav>
		<view class="header" style="height: 50px">
			<image class="back" src="/static/img/my-img/zjt.png" @click="back"></image>
			<text class="help">帮助</text>
		</view>
		<view class="body">
			<image class="bg" src="/static/img/loginbg.png" alt=""></image>
		</view>
		<u--input v-if="!type" placeholder="请输入账号" maxlength="11" border="surround" v-model="mobile"></u--input>
		<u--input v-if="type" placeholder="请输入密码" type="password" border="surround" v-model="password"></u--input>
		<button type="default" ></button>
		<button @click="login" class="btn">登录</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				type:false,
				mobile: '',
				password: ''
			};
		},

		methods: {
				
			back(){
				uni.navigateBack();
			},
			login() {
				// this.$api.login({
						// mobile: this.mobile,
						// password: this.password
					// },
					// (res) => {
						// if (res.data) {
							uni.setStorageSync('userToken', {
								mobile:this.mobile,
								password:this.password
							});
							
						// }
					// }
				// );
			}
		}
	};
</script>

<style lang="scss">
	.main {
		margin: 0 20px;

		.header {
			display: flex;
			align-items: center;
			justify-content: space-between;

			.back {
				width: 17rpx;
				height: 28rpx;
				margin-right: 26rpx;
			}

			.help {
				color: #333;
				font-size: 32rpx;
				font-weight: 600;
			}
		}
		.body{
			margin-top: 50rpx;
			margin-bottom: 580rpx;
			height: 300px;
			width: 100%;
			.bg{
				margin: 0 auto;
				height: 200px;
				// width: 150px;
				text-align: center;
			}
		}
		.btn{
			margin-top: 12rpx;
			background:#4575FA;
		}
	}
</style>