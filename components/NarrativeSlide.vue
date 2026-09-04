<script setup lang="ts">
defineProps<{
  number: string
  title: string
  image1: string
  image2: string
  image1Src?: string
  image2Src?: string
}>()
</script>

<template>
  <div class="narrative-slide">
    <div class="visual-grid">
      <div class="art-frame">
        <img v-if="image1Src" class="frame-image" :src="image1Src" :alt="image1" :title="image1">
        <template v-else>
          <div class="frame-id">{{ number }} A</div>
          <div class="frame-crosshair" aria-hidden="true"></div>
          <div class="frame-copy">{{ image1 }}</div>
        </template>
      </div>
      <div class="art-frame">
        <img v-if="image2Src" class="frame-image" :src="image2Src" :alt="image2" :title="image2">
        <template v-else>
          <div class="frame-id">{{ number }} B</div>
          <div class="frame-crosshair" aria-hidden="true"></div>
          <div class="frame-copy">{{ image2 }}</div>
        </template>
      </div>
    </div>

    <div class="story-panel">
      <div class="story-heading">
        <span>{{ number }}</span>
        <h2>{{ title }}</h2>
      </div>
      <div class="story-copy">
        <slot />
      </div>
    </div>
  </div>
</template>
