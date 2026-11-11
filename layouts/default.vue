<!-- ./layouts/default.vue -->
<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  siteUrl?: string
}>()

const liveDeckUrl = computed(() => {
  return props.siteUrl || 'https://github.com/yifanwo/vibe-coding-exhibition-slides#readme'
})
</script>

<template>
  <div class="slidev-layout default relative w-full h-full overflow-hidden">
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

    <div class="neo-default-content h-full overflow-y-auto pr-2">
      <slot />
    </div>
  </div>
</template>
