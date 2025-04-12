<template>
	<!-- App主页 -->
	<view class="page">
		<!-- 玩家卡片 -->
		<view class="player-card">
			<view class="nav-btn">
				<button v-if="currentHomePanel === 'function'" @click="currentHomePanel = 'player'">1</button>
				<button v-if="currentHomePanel === 'player'" @click="currentHomePanel = 'function'">0</button>
				<button @click="to">2</button>
			</view>
			<image class="avatar" src="/static/image/avatar-guest.png"></image>
			<text class="player-name">{{ name }}</text>
			<view>
				<text class="game-mode">osu!standard</text>
				<view class="pp">
					<text>1611</text>
					<text>{{ ' PP ' }}</text>
				</view>
				<text class="ranking">CN #1474</text>
			</view>
		</view>
		<!-- 二级页面 -->
		<view class="second-page">
			<!-- 功能面板 -->
			<FunctionPanel class="panel" v-show="currentHomePanel === 'function'"></FunctionPanel>
			<!-- 玩家信息面板 -->
			<PlayerPanel class="panel" v-show="currentHomePanel === 'player'"></PlayerPanel>
		</view>
	</view>
</template>

<script setup>
import { ref } from 'vue';
import FunctionPanel from './function/index';
import PlayerPanel from './player/index';
let name = ref('Player');
let currentHomePanel = ref('function');
function to() {
	uni.navigateTo({
		url: '/pages/settings',
	});
}
</script>

<style lang="scss" scoped>
.page {
	view.player-card {
		display: flex;
		position: relative;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: #002295;
		border-radius: 20rpx;
		box-shadow: 10rpx 10rpx 20rpx 20rpx rgba(0 0 0 / 0.2);
		margin: 15rpx 0;
		padding: 20rpx;
		row-gap: 20rpx;
		font-size: 40rpx;
		color: #fff;
		.nav-btn {
			position: absolute;
			display: flex;
			justify-content: space-between;
			z-index: 2;
			top: 20rpx;
			width: calc(100% - 40rpx);
			height: 40rpx;
			button {
				margin: 0;
				width: 40rpx !important;
				height: 40rpx;
				padding: 0;
				line-height: unset;
			}
		}
		.avatar {
			height: 200rpx;
			width: 200rpx;
			border-radius: 20rpx;
		}
		.player-name + view {
			width: 100%;
			position: relative;
			display: flex;
			justify-content: space-between;
			align-items: baseline;
			text-align: center;
			.game-mode {
				font-size: 18rpx !important;
			}
			view.pp {
				text:nth-child(1) {
					font-size: 60rpx !important;
					font-family: Torus-Bold, serif !important;
				}
				text:nth-child(2) {
					font-size: 40rpx !important;
					font-family: Torus-Bold, serif !important;
				}
			}
			.ranking {
				font-size: 18rpx !important;
			}
		}
	}
	view.second-page .panel {
		display: flex;
		flex-wrap: wrap;
		width: 100%;
		position: relative;
		row-gap: 15px;
		column-gap: 10px;
	}
}
</style>
