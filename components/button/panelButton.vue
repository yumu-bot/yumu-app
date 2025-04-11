<template>
	<!-- 主页面板按钮 -->
	<button class="panel">
		<view class="icon">
			<image></image>
		</view>
		<view class="title">
			<text>{{ btnName }}</text>
			<text>{{ btnSecondName }}</text>
		</view>
	</button>
</template>

<script setup name="panelButton">
const props = defineProps({
	btnName: String,
	btnSecondName: String,
	icon: String,
});
</script>

<style lang="scss" scoped>
.panel {
	width: calc(50% - 5px);
	box-shadow: 10rpx 10rpx 10rpx 10rpx rgba(0 0 0 / 0.2);
	border-radius: 20rpx;
	text-align: center;
	position: relative;
	padding: 0;
	line-height: unset;
	margin: 0;
	box-sizing: border-box;
	.icon {
		// height: 60%;
		border-radius: 20rpx;
		background: linear-gradient(to right, #1fd5fb, #5569bc);
		// z-index: 2;
		padding: 20rpx 0;
		image {
			width: 100rpx;
			height: 100rpx;
			border-radius: 50%;
			background-color: #fff;
		}
	}
	.title {
		// height: 40%;
		display: flex;
		flex-direction: column;
		padding: 10rpx 0;
		text:first-child {
			font-size: 40rpx;
			font-weight: bold;
		}
		text:last-child {
			font-size: 18rpx;
		}
	}
}
</style>
