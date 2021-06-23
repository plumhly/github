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
			<button type="default" @click="login">使用GitHub登录</button>
		</view>
		<uni-popup ref="popup" type="bottom">
			<view class="popup">
				<view class="popup_content">
					<view class="popup_head">
						<view>仓库访问权限选项</view>
						<view>隐私声明：PPHub不会从您的GitHub账号收集任何信息，我甚至连服务器都没有，请您放心使用。</view>
					</view>
					<button type="default" @click="onlyAllowPublicRepository">仅公开库</button>
					<button type="default" @click="allowAll">私有库 + 公开库</button>
				</view>
				<view class="popup_cance">
					<button type="default" @click="dismiss">取消</button>
				</view>
			</view>
		</uni-popup>
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
			login() {
				this.$refs.popup.open();
			},
			
			dismiss() {
				this.$refs.popup.close();
			},
			
			onlyAllowPublicRepository() {
				
			},
			
			allowAll() {
				
			},
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
				color: $uni-text-color;
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
		
		.popup {
			background-color: transparent;
			padding: 0 16rpx 16rpx;
			.popup_content {
				background-color: white;
				border-radius: 23rpx;
				overflow: hidden;
				color: $uni-text-color-grey;
				text-align: center;
				font-size: 27rpx;
				.popup_head {
					padding: 30rpx 38rpx 48rpx;
					view:first-child {
						font-weight: bold;
						margin-bottom: 17rpx;
					}
				}
								
				button {
					border-top: 1px solid $uni-border-color;
					border-radius: 0;
					color: $uni-text-color;
				}
				
				button:after { border: none }
			}
			
			.popup_cance {
				margin-top: 16rpx;
				font-size: 38rpx;
				font-weight: bold;
				
				button {
					height: 110rpx;
					line-height: 110rpx;
					text-align: center;
					color: $uni-text-color;
					border-radius: 23rpx;
				}
			}
		}
	}
	
</style>
