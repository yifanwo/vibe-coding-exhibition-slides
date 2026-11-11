<!-- layouts/split-showcase.vue -->
<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  ratio?: 'left-slim' | 'left-wide' | 'equal'
  spineTop?: string
  spineBottom?: string
  siteUrl?: string
}>()

// Automatically detects live URL in browser, or falls back to your planned GitHub Pages URL
const liveDeckUrl = computed(() => {
  if (props.siteUrl) return props.siteUrl
  if (typeof window !== 'undefined' && !window.location.hostname.includes('localhost') && !window.location.hostname.includes('127.0.0.1')) {
    return window.location.origin + window.location.pathname.replace(/\/\d+$/, '')
  }

  return 'https://github.com/yifanwo/vibe-coding-exhibition-slides#readme'
})

</script>

<template>
  <div class="slidev-layout split-showcase relative w-full h-full overflow-hidden">
    <!-- Single Full-Height Vertical Spine Bar (Never Overlaps!) -->
    <div class="neo-spine-bar">
      <span v-if="spineBottom !== ''" class="neo-spine-bottom">
        {{ spineBottom || '(Vibe)Coding for Curating a Web-Native Exhibition' }}
      </span>
      <span v-if="spineTop !== ''" class="neo-spine-top">
        {{ spineTop || '2026-11-05/Yifan WANG' }}
      </span>
    </div>

    <!-- Bottom-Right Clickable URL Stamp Bar -->
    <a
      :href="liveDeckUrl"
      target="_blank"
      rel="noopener noreferrer"
      class="neo-bottom-stamp"
    >
      🔗 {{ liveDeckUrl }}
    </a>

    <!-- Top Slide Header Slot (renders # Heading before ::left::) -->
    <div class="neo-slide-header">
      <slot />
    </div>

    <!-- Configurable Two-Column Split -->
    <div class="neo-split-layout" :class="ratio || 'left-slim'">
      <div class="neo-left-col">
        <slot name="left" />
      </div>
      <div class="neo-right-col">
        <slot name="right" />
      </div>
    </div>
  </div>

    <!-- Top Slide Header Slot (renders # Heading before ::left::) -->
    <div class="neo-slide-header">
      <slot />
    </div>

</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@500;700&family=Plus+Jakarta+Sans:ital,wght@0,400;0,500;0,700;0,800;1,600&family=Space+Grotesk:wght@600;700&family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@700;800&display=swap');

:root {
  --lotus-pink-top: #F6A8C9;
  --peach-blush: #F6C7D4;
  --silk-cream: #F8EFE0;
  --lower-rose: #F1A3C6;
  --celadon-mist: #DCECE3;
  --ivory-fade: #EFECE4;
  --carmine-rose: #D83B78;
  --deep-rose: #8C244E;
  --plum-ink: #3B1629;
  --plum-body: #5E2F46;
  --lotus-teal: #2E8584;
  --marker-pink: rgba(247, 178, 205, 0.72);
  --marker-celadon: rgba(188, 230, 214, 0.75);
}

.slidev-layout {
  background-color: var(--silk-cream) !important;
  color: var(--plum-ink) !important;
  font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif !important;
  position: relative !important;
  overflow: hidden !important;
  padding: 1.5rem 2.5rem 1.5rem 4.2rem !important;
  z-index: 1;
  border: none !important;
}

/* Layer 1: Multi-band atmospheric gradient */
.slidev-layout::before {
  content: "";
  position: absolute;
  inset: 0;
  pointer-events: none;
  z-index: -2;
  background-image:
    radial-gradient(ellipse 36% 30% at 68% 52%, rgba(220, 236, 227, 0.75) 0%, transparent 100%),
    radial-gradient(ellipse 20% 24% at 12% 22%, rgba(220, 236, 227, 0.45) 0%, transparent 100%),
    linear-gradient(
      180deg,
      rgba(246, 168, 201, 0.92) 0%,
      rgba(246, 199, 212, 0.62) 18%,
      rgba(248, 239, 224, 0.92) 34%,
      rgba(248, 239, 224, 0.92) 66%,
      rgba(241, 163, 198, 0.72) 78%,
      rgba(239, 236, 228, 0.96) 92%,
      rgba(239, 236, 228, 0.99) 100%
    );
}

/* Layer 2: Transparent Washi Fractal Noise */
.slidev-layout::after {
  content: "";
  position: absolute;
  inset: 0;
  pointer-events: none;
  z-index: -1;
  opacity: 0.30;
  mix-blend-mode: overlay;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 220 220' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='washiNoise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.88' numOctaves='3' stitchTiles='stitch'/%3E%3CfeColorMatrix type='matrix' values='1 0 0 0 0.04  0 1 0 0 0.02  0 0 1 0 0.03  0 0 0 0.42 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23washiNoise)'/%3E%3C/svg%3E");
}

/* Dreamy Custom Scrollbar (Soft Rose-Lotus Gradient Pill + Frosted Silk Track) */
.slidev-layout * {
  scrollbar-width: thin;
  scrollbar-color: rgba(216, 59, 120, 0.38) rgba(248, 239, 224, 0.35);
}

.slidev-layout ::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}

.slidev-layout ::-webkit-scrollbar-track {
  background: rgba(248, 239, 224, 0.4);
  border-radius: 999px;
  margin: 6px;
}

.slidev-layout ::-webkit-scrollbar-thumb {
  background: linear-gradient(180deg, rgba(246, 168, 201, 0.85) 0%, rgba(216, 59, 120, 0.55) 100%);
  border-radius: 999px;
  border: 1px solid rgba(250, 245, 238, 0.6);
}

.slidev-layout ::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(180deg, rgba(216, 59, 120, 0.85) 0%, rgba(140, 36, 78, 0.75) 100%);
}

/* Typography Hierarchy */
.slidev-layout h1 {
  font-family: 'Syne', 'Space Grotesk', sans-serif !important;
  font-weight: 800 !important;
  font-size: 1.85rem !important;
  letter-spacing: -0.03em !important;
  line-height: 1.08 !important;
  color: var(--carmine-rose) !important;
  margin-bottom: 0.45rem !important;
}

.slidev-layout h2,
.slidev-layout h3 {
  font-family: 'Space Grotesk', sans-serif !important;
  font-weight: 700 !important;
  font-size: 0.92rem !important;
  letter-spacing: -0.01em !important;
  color: var(--deep-rose) !important;
  margin-top: 0 !important;
  margin-bottom: 0.3rem !important;
}

.slidev-layout p,
.slidev-layout li {
  font-size: 0.74rem !important;
  line-height: 1.38 !important;
  color: var(--plum-body) !important;
  margin-top: 0.12rem !important;
  margin-bottom: 0.12rem !important;
}

.slidev-layout ul,
.slidev-layout ol {
  padding-left: 1.1rem !important;
  margin: 0.2rem 0 !important;
}

.slidev-layout blockquote {
  border-left: 3px solid var(--carmine-rose) !important;
  padding: 0.2rem 0.65rem !important;
  background: rgba(246, 199, 212, 0.28) !important;
  border-radius: 0 8px 8px 0 !important;
  font-weight: 700 !important;
  color: var(--plum-ink) !important;
  margin: 0.3rem 0 !important;
  width: fit-content !important;
  max-width: 100% !important;
}

.slidev-layout a {
  color: var(--carmine-rose) !important;
  font-weight: 700 !important;
  text-decoration: underline !important;
  text-underline-offset: 2px !important;
}

/* Switchable Two-Column Ratios */
.neo-slide-header {
  position: relative;
  z-index: 2;
  margin-bottom: 0.25rem;
}

.neo-split-layout {
  display: grid !important;
  grid-template-columns: 34% 1fr !important;
  gap: 1.25rem !important;
  height: calc(100% - 2.6rem) !important;
  align-items: stretch !important;
  position: relative;
  z-index: 2;
}

/* Format 1 (Default): Slimmer Left (34%) + Wider Right (66%) */
.neo-split-layout.left-slim {
  grid-template-columns: 34% 1fr !important;
}

/* Format 2: Wider Left (62%) + Slimmer Right (38%) */
.neo-split-layout.left-wide {
  grid-template-columns: 62% 1fr !important;
}

/* Format 3: Equal Columns (50% / 50%) */
.neo-split-layout.equal {
  grid-template-columns: 1fr 1fr !important;
}

.neo-left-col {
  background: rgba(250, 245, 238, 0.68);
  backdrop-filter: blur(8px);
  border-radius: 16px;
  padding: 0.75rem 0.95rem;
  height: 100%;
  overflow-y: auto;
  box-shadow: 0 8px 24px -6px rgba(216, 59, 120, 0.08);
}

.neo-right-col {
  background: rgba(250, 245, 238, 0.88);
  backdrop-filter: blur(14px);
  border-radius: 18px;
  padding: 0.75rem 1.1rem;
  height: 100%;
  overflow-y: auto;
  box-shadow: 0 12px 30px -6px rgba(216, 59, 120, 0.12);
}

/* Fix ASCII Box Diagrams & Code Blocks Inside Slidev */
.slidev-layout pre,
.slidev-code-wrapper pre,
.shiki {
  font-family: 'JetBrains Mono', 'Space Mono', monospace !important;
  font-size: 0.56rem !important;
  line-height: 1.12 !important;
  letter-spacing: 0 !important;
  font-variant-ligatures: none !important;
  background: rgba(248, 239, 224, 0.9) !important;
  color: var(--plum-ink) !important;
  padding: 0.5rem 0.7rem !important;
  border-radius: 10px !important;
  margin: 0.25rem 0 !important;
  overflow-x: auto !important;
}

/* Vertical Spine Bar: Single Flex Column so Top Date/Name & Bottom Title Never Overlap */
.neo-spine-bar {
  position: absolute;
  left: 0.95rem;
  top: 1.6rem;
  bottom: 1.6rem;
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1.25rem;
  pointer-events: none;
  z-index: 10;
}

.neo-spine-top {
  font-family: 'Space Mono', monospace;
  font-weight: 700;
  font-size: 0.64rem;
  letter-spacing: 0.06em;
  color: var(--deep-rose);
  opacity: 0.85;
  white-space: nowrap;
  flex-shrink: 0;
}

.neo-spine-bottom {
  font-family: 'Space Mono', monospace;
  font-weight: 700;
  font-size: 0.62rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: var(--carmine-rose);
  opacity: 0.85;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.neo-mark {
  background: var(--marker-pink);
  color: var(--plum-ink);
  font-weight: 800;
  padding: 0.08rem 0.35rem;
  border-radius: 4px;
}

.dream-pill {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  font-family: 'Space Mono', monospace;
  font-weight: 700;
  font-size: 0.75rem;
  padding: 0.3rem 1rem;
  border-radius: 999px;
  background: var(--carmine-rose);
  color: var(--silk-cream);
}

.neo-browser-window {
  background: rgba(250, 245, 238, 0.95);
  border-radius: 14px;
  overflow: hidden;
  box-shadow: 0 8px 22px -6px rgba(216, 59, 120, 0.14);
}

.neo-browser-toolbar {
  background: rgba(243, 220, 230, 0.88);
  padding: 0.3rem 0.75rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.neo-browser-dots {
  display: flex;
  gap: 0.25rem;
}

.neo-browser-dots span {
  width: 7px;
  height: 7px;
  border-radius: 999px;
  display: inline-block;
}

.neo-browser-url {
  background: rgba(250, 245, 238, 0.92);
  border-radius: 999px;
  padding: 0.1rem 0.65rem;
  font-family: 'Space Mono', monospace;
  font-size: 0.58rem;
  font-weight: 700;
  color: var(--deep-rose);
  flex: 1;
}

/* Automatically stamps the Title + Date + Name bar onto EVERY slide layout except the Cover */
.slidev-page:not(.slidev-page-1) .slidev-layout {
  background-image: none; /* keeps pseudo-elements clean */
}

/* Global Spine via global-top.vue OR fallback */
.neo-global-spine {
  position: absolute;
  left: 0.95rem;
  top: 1.6rem;
  bottom: 1.6rem;
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1.25rem;
  pointer-events: none;
  z-index: 100;
}

.neo-box {
  display: inline-block;
  border: 1.5px solid var(--carmine-rose);
  background: rgba(250, 245, 238, 0.9);
  color: var(--plum-ink);
  font-weight: 800;
  padding: 0.04rem 0.42rem;
  border-radius: 3px;
  line-height: 1.2;
}

.neo-kbd {
  display: inline-block;
  font-family: 'Space Mono', monospace;
  font-size: 0.7rem;
  font-weight: 700;
  border: 1.5px solid var(--plum-ink);
  background: var(--silk-cream);
  color: var(--plum-ink);
  padding: 0.04rem 0.42rem;
  border-radius: 4px;
  box-shadow: 2px 2px 0px var(--carmine-rose);
}

/* Bottom-Right URL Stamp Bar */
.neo-bottom-stamp {
  position: absolute;
  right: 2.5rem;
  bottom: 0.45rem;
  font-family: 'Space Mono', monospace;
  font-weight: 700;
  font-size: 0.58rem;
  letter-spacing: 0.04em;
  color: var(--deep-rose) !important;
  text-decoration: none !important;
  opacity: 0.75;
  z-index: 20;
  transition: opacity 0.15s ease;
}

.neo-bottom-stamp:hover {
  opacity: 1;
  text-decoration: underline !important;
}


</style>
