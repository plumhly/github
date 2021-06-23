<template>
	<view class="container">
		<view class="access">
			<text>Access Token</text>
		</view>
		<view class="logo">
			<image src="/static/logo.png" mode="aspectFit"></image>
			<view>PPHub For Github</view>
		</view>
		
		<view class="bottom_container">
			<button type="default">使用GitHub登录</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
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
		height: 100%;
	}
	
	.container {
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		.access {
			width: 100%;
			text {
				float: right;
				font-size: 24rpx;
				color: #027cff;
				margin: 40rpx 24rpx 0 0;
			}
		}
		
		.logo {
			padding-bottom: 80rpx;
			view {
				margin-top: 40px;
				text-align: center;
				font-size: 28rpx;
				color: #323b4b;
			}
		}
		
		.bottom_container {
			width: 100%;
			padding-bottom: 90px;
			button {
				margin: 0 69px;
				color: white;
				background-color: #434a53;
				border-radius: 14px;
			}
		}
		
	}
	
</style>
