<template>
	<!-- 主页面板按钮组件 -->
	<button class="panel">
		<view class="icon" :style="iconBgStyle">
			<image :src="icon"></image>
		</view>
		<view class="title">
			<text>{{ btnName }}</text>
			<text>{{ btnSecondName }}</text>
		</view>
	</button>
</template>

<script setup name="panelButton">
const props = defineProps({
	btnName: String, // 按钮名称
	btnSecondName: String, // 按钮次名称/副标题
	icon: String, // 图标
	iconBgStyle: { type: String, default: 'background: linear-gradient(to right, #1fd5fb, #5569bc)' }, // 图标背景自定义样式
});
</script>

<style lang="scss" scoped>
.panel {
	width: calc(50% - 5rpx);
	height: 220rpx;
	max-height: 220rpx;
	box-shadow: 5rpx 5rpx 5rpx 5rpx rgba(0, 0, 0, 0.2);
	border-radius: 20rpx;
	text-align: center;
	position: relative;
	padding: 0;
	line-height: unset;
	margin: 0;
	box-sizing: border-box;
	overflow: visible;
	&::after {
		border: 0;
	}
	.icon {
		// height: 60%;
		width: calc(100% + 0.1rpx);
		border-radius: 20rpx;
		position: relative;
		padding: 20rpx 0;
		image {
			width: 100rpx;
			height: 100rpx;
		}
	}
	.title {
		// height: 40%;
		display: flex;
		flex-direction: column;
		padding: 0rpx 0;
		box-sizing: border-box;
		text:first-child {
			font-size: 30rpx;
			font-weight: bold;
		}
		text:last-child {
			font-size: 18rpx;
		}
	}
}
</style>
