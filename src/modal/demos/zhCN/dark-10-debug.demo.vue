<markdown>
# pop debug 5
</markdown>

<script lang="ts" setup>
import { ref } from 'vue'

const modalActive = ref(false)
</script>

<template>
  <n-popover trigger="click">
    <template #trigger>
      <n-button @click="modalActive = !modalActive">
        Toggle
      </n-button>
    </template>
    <n-table :bordered="false" :single-line="false">
      <thead>
        <tr>
          <th>Abandon</th>
          <th>Abnormal</th>
          <th>Abolish</th>
          <th>...</th>
          <th>It's hard to learn words</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>放弃</td>
          <td>反常的</td>
          <td>彻底废除</td>
          <td>...</td>
          <td>Damn it! I can't remember those words.</td>
        </tr>
        <tr>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
          <td>...</td>
        </tr>
      </tbody>
    </n-table>
    <n-list>
      <template #header>
        hhh
      </template>
      <template #footer>
        fff
      </template>
      <n-list-item>
        <template #prefix>
          <n-button>Prefix</n-button>
        </template>
        <template #suffix>
          <n-button>Suffix</n-button>
        </template>
        <n-thing title="Thing" title-extra="extra" description="description">
          Biu<br>
          Biu<br>
          Biu<br>
        </n-thing>
      </n-list-item>
      <n-list-item>
        <n-thing title="Thing" title-extra="extra" description="description">
          Biu<br>
          Biu<br>
          Biu<br>
        </n-thing>
        <template #suffix>
          <n-button>Suffix</n-button>
        </template>
      </n-list-item>
    </n-list>
    <n-list bordered>
      <template #header>
        hhh
      </template>
      <template #footer>
        fff
      </template>
      <n-list-item>
        <template #prefix>
          <n-button>Prefix</n-button>
        </template>
        <template #suffix>
          <n-button>Suffix</n-button>
        </template>
        <n-thing title="Thing" title-extra="extra" description="description">
          Biu<br>
          Biu<br>
          Biu<br>
        </n-thing>
      </n-list-item>
      <n-list-item>
        <n-thing title="Thing" title-extra="extra" description="description">
          Biu<br>
          Biu<br>
          Biu<br>
        </n-thing>
        <template #suffix>
          <n-button>Suffix</n-button>
        </template>
      </n-list-item>
    </n-list>
    <n-descriptions bordered>
      <n-descriptions-item>
        <template #label>
          Breakfast
        </template>
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Lunch">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Supper">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
    </n-descriptions>
    <n-descriptions label-placement="left" bordered>
      <n-descriptions-item>
        <template #label>
          Breakfast
        </template>
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Lunch">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Supper">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
    </n-descriptions>
    <n-descriptions>
      <n-descriptions-item>
        <template #label>
          Breakfast
        </template>
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Lunch">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Supper">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
    </n-descriptions>
    <n-descriptions label-placement="left">
      <n-descriptions-item>
        <template #label>
          Breakfast
        </template>
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Lunch">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Supper">
        Apple
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
      <n-descriptions-item label="Why Long">
        Why <br>
        Long <br>
        Long <br>
        Long <br>
        Long <br>
        Long
      </n-descriptions-item>
    </n-descriptions>
  </n-popover>
</template>
