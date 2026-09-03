<script setup lang="ts">
defineProps<{
  number: string
  title: string
  image: string
}>()
</script>

<template>
  <div class="narrative-slide">
    <div class="art-frame">
      <div class="frame-id">IMAGE {{ number }}</div>
      <div class="frame-crosshair" aria-hidden="true"></div>
      <div class="frame-copy">{{ image }}</div>
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
