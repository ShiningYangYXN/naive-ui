<markdown>
# Group

A radio group looks elegant.
</markdown>

<script lang="ts" setup>
import { ref } from 'vue'

const value = ref(null)
const songs = [
  {
    value: 'Rock\'n\'Roll Star',
    label: 'Rock\'n\'Roll Star'
  },
  {
    value: 'Shakermaker',
    label: 'Shakermaker'
  },
  {
    value: 'Live Forever',
    label: 'Live Forever'
  },
  {
    value: 'Up in the Sky',
    label: 'Up in the Sky'
  },
  {
    value: '...',
    label: '...'
  }
].map((s) => {
  s.value = s.value.toLowerCase()
  return s
})
</script>

<template>
  <n-radio-group v-model:value="value" name="radiogroup">
    <n-space>
      <n-radio
        v-for="song in songs"
        :key="song.value"
        :value="song.value"
        :label="song.label"
      />
    </n-space>
  </n-radio-group>
</template>
