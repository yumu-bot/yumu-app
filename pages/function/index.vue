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
		iconBgStyle: 'background: linear-gradient(150deg, #1fd5fb, #5569bc)',
	},
	{
		name: '查询最好成绩',
		note: 'Get Best Scores',
		icon: '/static/image/svg/crown-solid.svg',
		iconBgStyle: 'background: linear-gradient(150deg, #f47f77, #b7345f)',
	},
	{
		name: '查询谱面成绩',
		note: 'Get Beatmap Scores',
		icon: '/static/image/svg/map-location-dot-solid.svg',
		iconBgStyle: 'background: linear-gradient(150deg, #feda47, #fb7298)',
	},
	{
		name: '分析最好成绩',
		note: 'Best Performance Analysis v3',
		icon: '/static/image/svg/flask-vial-solid.svg',
		iconBgStyle: 'background: linear-gradient(150deg, #FDE997, #E355DF)',
	},
	{
		name: '查询排行榜',
		note: 'Get Leaderboard',
		icon: '/static/image/svg/list-ol-solid.svg',
		iconBgStyle: 'background: linear-gradient(150deg, #2871FA, #671ACE)',
	},
	{
		name: '搜索谱面',
		note: 'Search Beatmap',
		icon: '/static/image/svg/magnifying-glass.svg',
		iconBgStyle: 'background: linear-gradient(150deg, #39F7CD, #43EA80)',
	},
]);
</script>

<style lang="scss"></style>
