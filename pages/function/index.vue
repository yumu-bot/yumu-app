<template>
  <!-- 功能面板 -->
  <view>
    <PanelButton v-for="(item, index) in functionList" :btnName="item.name" :btnSecondName="item.note"></PanelButton>
  </view>
</template>

<script setup name="FunctionPanel">
import {ref} from 'vue';
import PanelButton from '@/components/button/panelButton';

const functionList = ref([
  {
    name: '查询最近成绩',
    note: 'Get Recent Scores',
    icon: '/',
  },
  {
    name: '查询最好成绩',
    note: 'Get Best Scores',
    icon: ''
  },
  {
    name: '查询谱面成绩',
    note: 'Get Beatmap Scores',
    icon: ''},
]);
</script>

<style lang="scss"></style>
