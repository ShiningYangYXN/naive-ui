<markdown>
# Modify exist message
</markdown>

<script lang="ts" setup>
import type { MessageReactive, MessageType } from 'naive-ui'
import { useMessage } from 'naive-ui'
import { ref } from 'vue'

const message = useMessage()
const types: MessageType[] = ['success', 'info', 'warning', 'error', 'loading']
const countRef = ref(0)
let typeIndex = 0
let msgReactive: MessageReactive | null = null

function plus() {
  if (msgReactive) {
    countRef.value++
    msgReactive.content = `${countRef.value}`
  }
}

function changeType() {
  if (msgReactive) {
    typeIndex = (typeIndex + 1) % types.length
    msgReactive.type = types[typeIndex]
  }
}

function createMessage() {
  msgReactive = message.create(`${countRef.value}`, {
    type: types[typeIndex],
    duration: 10000
  })
}
</script>

<template>
  <n-space>
    <n-button @click="createMessage">
      Create a Message Firstly
    </n-button>
    <n-button @click="changeType">
      Change Type
    </n-button>
    <n-button @click="plus">
      Plus 1
    </n-button>
  </n-space>
</template>
