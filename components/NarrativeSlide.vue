<script setup lang="ts">
defineProps<{
  number: string
  title: string
  image1: string
  image2: string
}>()
</script>

<template>
  <div class="narrative-slide">
    <div class="visual-grid">
      <div class="art-frame">
        <div class="frame-id">{{ number }} A</div>
        <div class="frame-crosshair" aria-hidden="true"></div>
        <div class="frame-copy">{{ image1 }}</div>
      </div>
      <div class="art-frame">
        <div class="frame-id">{{ number }} B</div>
        <div class="frame-crosshair" aria-hidden="true"></div>
        <div class="frame-copy">{{ image2 }}</div>
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
