<markdown>
# Unkeyed
</markdown>

<script lang="ts" setup>
const list = [
  {
    a: '1a',
    b: '1b'
  },
  {
    a: '2a',
    b: '2b'
  },
  {
    a: '3a',
    b: '3b'
  }
]
</script>

<template>
  <n-tabs type="line" :default-value="list[0].a">
    <!-- eslint-disable vue/valid-v-for -->
    <n-tab-pane v-for="i in list" :name="i.a" :tab="i.b">
      <div>{{ i.a }} {{ i.b }}</div>
    </n-tab-pane>
  </n-tabs>
</template>
