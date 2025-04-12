<template>
	<!-- 功能面板 -->
	<view>
		<PanelButton v-for="(item, index) in functionList" :btnName="item.name" :btnSecondName="item.note" :icon="item.icon" :iconBgStyle="item.iconBgStyle"></PanelButton>
	</view>
</template>

<script setup name="FunctionPanel">
import { ref } from 'vue';
import PanelButton from '@/components/button/panelButton';

const functionList = ref([
	{
		name: '查询最近成绩',
		note: 'Get Recent Scores',
		icon: '/static/image/svg/splotch-solid.svg',
		iconBgStyle: 'background: linear-gradient(to right, #1fd5fb, #5569bc)',
	},
	{
		name: '查询最好成绩',
		note: 'Get Best Scores',
		icon: '/static/image/svg/crown-solid.svg',
		iconBgStyle: 'background: linear-gradient(to right, #f47f77, #b7345f)',
	},
	{
		name: '查询谱面成绩',
		note: 'Get Beatmap Scores',
		icon: '/static/image/svg/map-location-dot-solid.svg',
		iconBgStyle: 'background: linear-gradient(to right, #feda47, #fb7298)',
	},
]);
</script>

<style lang="scss"></style>
