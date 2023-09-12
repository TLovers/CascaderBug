<script setup lang="ts">
import 'ant-design-vue/dist/antd.css';
import {Cascader} from 'ant-design-vue'
import type { CascaderProps } from 'ant-design-vue';
const options: CascaderProps['options'] = [
  {
    value: 'zhejiang',
    label: 'Zhejiang',
    children: [
      {
        value: 'hangzhou',
        label: 'Hangzhou',
        children: [
          {
            value: 'xihu',
            label: 'West Lake',
          },
        ],
      },
    ],
  },
  {
    value: 'jiangsu',
    label: 'Jiangsu',
    children: [
      {
        value: 'nanjing',
        label: 'Nanjing',
        children: [
          {
            value: 'zhonghuamen',
            label: 'Zhong Hua Men',
          },
        ],
      },
    ],
  },
];
const value =ref<string[]>([])
</script>
<template>
  <div>
    <Cascader v-model:value="value" :options="options" placeholder="Please select" />
  </div>
</template>
