<markdown>
# 卡片类型

设定 `type='card'`。
</markdown>

<script lang="ts" setup>
import { useMessage } from 'naive-ui'
import { ref } from 'vue'

const nameRef = ref(1)
const message = useMessage()
const panelsRef = ref([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15])

function handleClose(name: number) {
  const { value: panels } = panelsRef
  if (panels.length === 1) {
    message.error('最后一个了')
    return
  }
  message.info(`关掉 ${name}`)
  const index = panels.findIndex(v => name === v)
  panels.splice(index, 1)
  if (nameRef.value === name) {
    nameRef.value = panels[index]
  }
}

const name = nameRef
const panels = panelsRef
</script>

<template>
  <n-tabs
    v-model:value="name"
    type="card"
    closable
    tab-style="min-width: 80px;"
    @close="handleClose"
  >
    <n-tab-pane
      v-for="panel in panels"
      :key="panel"
      :tab="panel.toString()"
      :name="panel"
    >
      {{ panel }}
    </n-tab-pane>
  </n-tabs>
</template>
