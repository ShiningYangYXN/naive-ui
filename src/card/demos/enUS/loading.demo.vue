<markdown>
# Loading

Use `n-skeleton` to simulate loading effect.
</markdown>

<script setup lang="ts">
import { ref } from 'vue'

const loading = ref(true)
</script>

<template>
  <n-space vertical>
    <n-switch v-model:value="loading" />
    <n-card>
      <template #header>
        <n-skeleton v-if="loading" text width="60%" />
        <template v-else>
          Lorem Ipsum
        </template>
      </template>
      <n-skeleton v-if="loading" text :repeat="6" />
      <template v-else>
        Lorem ipsum dolor sit amet,<br>
        consectetur adipiscing elit,<br>
        sed do eiusmod tempor incididunt<br>
        ut labore et dolore magna aliqua.<br>
        Ut enim ad minim veniam,<br>
        quis nostrud exercitation ullamco
      </template>
    </n-card>
  </n-space>
</template>
