<markdown>
# Dots

Set `dot-type` to change the style of the dots. You can use `:show-dots="false"` to hide the dots.

Set `dot-placement` to change the position of the dots.
</markdown>

<script lang="ts" setup>
import { ref } from 'vue'

const typeRef = ref<'dot' | 'line'>('dot')
const placementRef = ref<'top' | 'bottom' | 'left' | 'right'>('bottom')
const directionRef = ref<'horizontal' | 'vertical'>('horizontal')
const showArrow = ref(false)
const type = typeRef
const types = ['dot', 'line']
const placement = placementRef
const placements = ['top', 'bottom', 'left', 'right']
const direction = directionRef
const directions = ['horizontal', 'vertical']
</script>

<template>
  <n-space vertical>
    <n-radio-group v-model:value="type">
      <n-radio-button v-for="_type in types" :key="_type" :value="_type">
        {{ _type }}
      </n-radio-button>
    </n-radio-group>
    <n-radio-group v-model:value="placement">
      <n-radio-button
        v-for="_placement in placements"
        :key="_placement"
        :value="_placement"
      >
        {{ _placement }}
      </n-radio-button>
    </n-radio-group>
    <n-radio-group v-model:value="direction">
      <n-radio-button
        v-for="_direction in directions"
        :key="_direction"
        :value="_direction"
      >
        {{ _direction }}
      </n-radio-button>
    </n-radio-group>
    <n-switch v-model:value="showArrow">
      <template #checked>
        Show arrow
      </template>
      <template #unchecked>
        No arrow
      </template>
    </n-switch>
    <n-carousel
      :direction="direction"
      :show-arrow="showArrow"
      :dot-type="type"
      :dot-placement="placement"
      style="height: 240px"
    >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel1.jpeg"
      >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg"
      >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel3.jpeg"
      >
      <img
        class="carousel-img"
        src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel4.jpeg"
      >
    </n-carousel>
  </n-space>
</template>

<style>
.carousel-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
