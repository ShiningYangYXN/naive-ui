<markdown>
# 操作插槽

有人要在选择菜单里用这个插槽吗？
</markdown>

<script lang="ts" setup>
import { ref } from 'vue'

const value = ref(null)
const options = [
  {
    label: 'Everybody\'s Got Something to Hide Except Me and My Monkey',
    value: 'song0',
    disabled: true
  },
  {
    label: 'Drive My Car',
    value: 'song1'
  },
  {
    label: 'Norwegian Wood',
    value: 'song2'
  },
  {
    label: 'You Won\'t See',
    value: 'song3',
    disabled: true
  }
]
</script>

<template>
  <n-select v-model:value="value" :options="options">
    <template #header>
      不知道放些什么
    </template>
    <template #action>
      如果你点开了这个例子，你可能需要它
    </template>
  </n-select>
</template>
