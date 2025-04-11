<template>
	<!-- App主页 -->
	<view class="page">
		<!-- 玩家卡片 -->
		<view class="player-card">
			<image class="avatar" src="/static/image/avatar-guest.png"></image>
			<text class="player-name">{{ title }}</text>
			<text>
				<text>1611</text>
				PP
			</text>
		</view>
		<!-- 二级页面 -->
		<view>
			<button type="default">测试按钮1</button>
			<button type="default">test2</button>
		</view>
	</view>
</template>

<script setup>
import { ref } from 'vue';
let title = ref('Player');
</script>

<style lang="scss">
.page {
	view.player-card {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: #002295;
		border-radius: 20rpx;
		box-shadow: 10rpx 10rpx 20rpx 20rpx rgba(0 0 0 / 0.2);
		margin: 15rpx 0;
		padding: 20rpx 0;
		row-gap: 20rpx;
		font-size: $uni-font-size-lg;
		color: #fff;
		.avatar {
			height: 200rpx;
			width: 200rpx;
		}
		.player-name + text {
			text {
				font-size: 20px !important;
			}
		}
	}
}

.text-area {
	display: flex;
	justify-content: center;
}

.title {
	font-size: 36rpx;
	color: #8f8f94;
}
</style>
