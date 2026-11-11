<!-- ./layouts/center.vue -->
<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  siteUrl?: string
}>()

const liveDeckUrl = computed(() => {
  if (props.siteUrl) return props.siteUrl
  if (
    typeof window !== 'undefined' &&
    !window.location.hostname.includes('localhost') &&
    !window.location.hostname.includes('127.0.0.1')
  ) {
    return window.location.origin + window.location.pathname.replace(/\/\d+$/, '')
  }
  return 'https://yifanwo.github.io/vibe-coding-exhibition-slides/'
})
</script>

<template>
  <div class="slidev-layout center relative w-full h-full overflow-hidden flex flex-col items-center justify-center text-center">
    <!-- Left Vertical Spine Bar (Hidden on Cover Page 1) -->
    <div v-if="$page !== 1" class="neo-spine-bar">
      <span class="neo-spine-bottom">
        (Vibe)Coding for Curating a Web-Native Exhibition
      </span>
      <span class="neo-spine-top">
        2026-11-05/Yifan WANG
      </span>
    </div>

    <!-- Bottom-Right Clickable URL Stamp Bar (Hidden on Cover Page 1) -->
    <a
      v-if="$page !== 1"
      :href="liveDeckUrl"
      target="_blank"
      rel="noopener noreferrer"
      class="neo-bottom-stamp"
    >
      🔗 {{ liveDeckUrl }}
    </a>

    <div class="my-auto">
      <slot />
    </div>
  </div>
</template>
