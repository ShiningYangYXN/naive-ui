<markdown>
# Action slot

Maybe you need to use this slot in the tree selection menu.
</markdown>

<script lang="ts" setup>
import type { TreeSelectOption } from 'naive-ui'

function handleUpdateValue(
  value: string | number | Array<string | number> | null,
  option: TreeSelectOption | null | Array<TreeSelectOption | null>
) {
  console.log(value, option)
}

const options = [
  {
    label: 'Rubber Soul',
    key: 'Rubber Soul',
    children: [
      {
        label: 'Everybody\'s Got Something to Hide Except Me and My Monkey',
        key: 'Everybody\'s Got Something to Hide Except Me and My Monkey'
      },
      {
        label: 'Drive My Car',
        key: 'Drive My Car',
        disabled: true
      },
      {
        label: 'Norwegian Wood',
        key: 'Norwegian Wood'
      },
      {
        label: 'You Won\'t See',
        key: 'You Won\'t See',
        disabled: true
      },
      {
        label: 'Nowhere Man',
        key: 'Nowhere Man'
      },
      {
        label: 'Think For Yourself',
        key: 'Think For Yourself'
      },
      {
        label: 'The Word',
        key: 'The Word'
      },
      {
        label: 'Michelle',
        key: 'Michelle',
        disabled: true
      },
      {
        label: 'What goes on',
        key: 'What goes on'
      },
      {
        label: 'Girl',
        key: 'Girl'
      },
      {
        label: 'I\'m looking through you',
        key: 'I\'m looking through you'
      },
      {
        label: 'In My Life',
        key: 'In My Life'
      },
      {
        label: 'Wait',
        key: 'Wait'
      }
    ]
  }
]
</script>

<template>
  <n-tree-select
    :options="options"
    default-value="Drive My Car"
    @update:value="handleUpdateValue"
  >
    <template #header>
      Don't know what to put
    </template>
    <template #action>
      You can customize some operations here.
    </template>
  </n-tree-select>
</template>
