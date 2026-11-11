<!-- ./components/WebPreview.vue -->
<script setup lang="ts">
defineProps<{
  src: string
  height?: string
}>()
</script>

<template>
  <div class="neo-browser-window my-2">
    <div class="neo-browser-toolbar">
      <div class="neo-browser-dots">
        <span class="bg-[#D83B78]"></span>
        <span class="bg-[#E89954]"></span>
        <span class="bg-[#3E8E8D]"></span>
      </div>
      <a
        :href="src"
        target="_blank"
        rel="noopener noreferrer"
        class="neo-browser-url truncate !no-underline hover:opacity-80"
        title="Click to open webpage in new tab"
      >
        {{ src }} ↗
      </a>
    </div>

    <!-- Outer frame clips to your requested height (h-36, h-44, h-52, h-64) -->
    <div class="neo-browser-body relative overflow-hidden !p-0" :class="height || 'h-48'">
      <!-- Inner iframe renders at 200% Desktop size and scales down by 50% (0.5) -->
      <iframe
        :src="src"
        class="neo-zoomed-iframe"
        loading="lazy"
      ></iframe>
    </div>
  </div>
</template>

<style scoped>
.neo-zoomed-iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 200%;
  height: 200%;
  transform: scale(0.53);
  transform-origin: top left;
  border: 0;
}
</style>
