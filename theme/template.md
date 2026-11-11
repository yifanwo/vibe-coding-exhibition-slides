---
theme: default
title: Mermaid Dream — Asymmetric Two-Column Text-Heavy & Diagram Slidev Deck
info: |
  Editorial Neobrutalist Two-Column Slidev Template
  Slimmer Left Column (Structured Dense Text) + Wider Right Column (Diagrams & Webpage Previews)
fonts:
  sans: 'Plus Jakarta Sans'
  display: 'Syne'
  mono: 'Space Mono'
  weights: '400,500,700,800'
css: unocss
---

<style src="./style.css"></style>

<!-- Vertical Left Margin Spine (Inspired by Reference 1: 2024/25 & INDEX) -->
<div class="neo-spine-top">2025/26</div>
<div class="neo-spine-bottom">INDEX // 01</div>

<!-- Giant Watermark Numeral in Background (Inspired by Reference 2: Giant '3') -->
<div class="neo-watermark-num">01</div>

<!-- Top Running Header Metadata -->
<div class="flex justify-between items-center text-[10px] font-bold tracking-widest uppercase text-[#8C244E] mb-3 font-mono">
  <span>GCO6001-20 // ARCHITECTURE & LIVE PREVIEW</span>
  <span>CHAPTER TWO: REFRAMING RESEARCH</span>
</div>

<!-- Asymmetric Two-Column Split: Slimmer Left (36%) + Wider Right (64%) -->
<div class="neo-split-layout">

  <!-- SLIMMER LEFT COLUMN: Heavy Stacked Headline + Pullquote + Indexed Sections -->
  <div class="flex flex-col justify-between pr-1">
    <div>
      <!-- Stacked Neobrutalist Display Headline -->
      <div class="neo-stacked-title">
        <span class="accent">System</span><br/>
        <span class="ink">Topology,</span><br/>
        <span class="accent">Live States</span>
      </div>

      <!-- Bold Pull-Quote Callout -->
      <div class="neo-pullquote">
        “Decouple state mutation from view rendering to keep global latency under 12ms.”
      </div>
    </div>

    <!-- Dense Structured Sections (Inspired by SECTION 0.1 / 0.2 / 0.3 + Marker Highlights) -->
    <div>
      <!-- SECTION 0.1 -->
      <div class="neo-section-block">
        <div class="neo-section-header">
          <div>
            <span class="neo-section-kicker">SECTION</span>
            <div class="neo-section-title">EDGE INGESTION PIPELINE</div>
          </div>
          <span class="neo-section-num">0.1</span>
        </div>
        <div class="neo-sublist">
          <div class="neo-subrow">
            <span class="key">Stream Router</span>
            <span class="desc">Zero-copy WebSocket frames</span>
            <span class="metric">04 ms</span>
          </div>
          <div class="neo-subrow">
            <span class="key">Schema Guard</span>
            <span class="desc">Strict runtime payload check</span>
            <span class="metric">02 ms</span>
          </div>
          <div class="neo-subrow highlight">
            <span class="key">Key Takeaway: 99.4% cache hit ratio on edge</span>
            <span class="metric">FAST</span>
          </div>
        </div>
      </div>

      <!-- SECTION 0.2 -->
      <div class="neo-section-block">
        <div class="neo-section-header">
          <div>
            <span class="neo-section-kicker">SECTION</span>
            <div class="neo-section-title">REACTIVE GRAPH ENGINE</div>
          </div>
          <span class="neo-section-num">0.2</span>
        </div>
        <div class="neo-sublist">
          <div class="neo-subrow">
            <span class="key">DAG Scheduler</span>
            <span class="desc">Parallel worker pool</span>
            <span class="metric">128x</span>
          </div>
          <div class="neo-subrow">
            <span class="key">State Snapshot</span>
            <span class="desc">Incremental CRDT delta sync</span>
            <span class="metric">SYNC</span>
          </div>
          <div class="neo-subrow highlight">
            <span class="key">Core Bottleneck: Eliminated lock contention</span>
            <span class="metric">ZERO</span>
          </div>
        </div>
      </div>

      <!-- SECTION 0.3 -->
      <div class="neo-section-block !mb-0">
        <div class="neo-section-header">
          <div>
            <span class="neo-section-kicker">SECTION</span>
            <div class="neo-section-title">VIEWPORT HYDRATION</div>
          </div>
          <span class="neo-section-num">0.3</span>
        </div>
        <div class="neo-sublist">
          <div class="neo-subrow">
            <span class="key">Island Stream</span>
            <span class="desc">Progressive DOM chunking</span>
            <span class="metric">SSR</span>
          </div>
          <div class="neo-subrow">
            <span class="key">Client Resume</span>
            <span class="desc">Instant interactive binding</span>
            <span class="metric">0.8s</span>
          </div>
          <div class="neo-subrow highlight">
            <span class="key">Production SLA: P99 under 15ms globally</span>
            <span class="metric">PASS</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- WIDER RIGHT COLUMN: Embedded Diagram Stage + Webpage Live Preview -->
  <div class="neo-right-stack">

    <!-- Top Container: Embedded Diagram Stage (Supports Mermaid / SVG / Custom Graphs) -->
    <div class="neo-diagram-stage">
      <div class="flex justify-between items-center mb-2">
        <span class="px-2.5 py-0.5 rounded-full bg-[#2E8584]/15 text-[#2E8584] font-mono text-[10px] font-bold">
          FIG 01 // MERMAID DIAGRAM
        </span>
        <span class="font-mono text-[10px] font-bold text-[#8C244E]">LIVE ARCHITECTURE GRAPH</span>
      </div>

      <!-- Clean Responsive SVG / Mermaid Diagram Area -->
      <div class="grid grid-cols-3 gap-3 items-center my-auto py-1">
        <div class="p-3 rounded-2xl bg-[#F6C7D4]/65">
          <div class="text-xs font-extrabold text-[#D83B78]">0.1 Edge Router</div>
          <div class="font-mono text-[10px] text-[#5E2F46] mt-1">WebSocket Ingest<br/>4.2M req/s</div>
        </div>
        <div class="space-y-2">
          <div class="p-2.5 rounded-2xl bg-[#DCECE3]/80">
            <div class="text-xs font-extrabold text-[#2E8584]">0.2a DAG Worker</div>
            <div class="font-mono text-[10px] text-[#5E2F46]">Parallel Compute</div>
          </div>
          <div class="p-2.5 rounded-2xl bg-[#DCECE3]/80">
            <div class="text-xs font-extrabold text-[#2E8584]">0.2b CRDT Store</div>
            <div class="font-mono text-[10px] text-[#5E2F46]">Zero-Lock State</div>
          </div>
        </div>
        <div class="p-3 rounded-2xl bg-[#F4A8C8]/65">
          <div class="text-xs font-extrabold text-[#3B1629]">0.3 SSR Islands</div>
          <div class="font-mono text-[10px] text-[#5E2F46] mt-1">Hydrated Viewport<br/>P99 &lt; 12ms</div>
        </div>
      </div>
    </div>

    <!-- Bottom Container: Embedded Webpage / Iframe Preview Window -->
    <div class="neo-browser-window">
      <div class="neo-browser-toolbar">
        <div class="neo-browser-dots">
          <span class="bg-[#D83B78]"></span>
          <span class="bg-[#E89954]"></span>
          <span class="bg-[#3E8E8D]"></span>
        </div>
        <div class="neo-browser-url">https://localhost:3000/live-telemetry-preview</div>
        <span class="font-mono text-[10px] font-bold text-[#D83B78]">IFRAME // INTERACTIVE</span>
      </div>

      <!-- You can drop an actual <iframe src="..." class="w-full h-full border-0" /> here, or rich HTML preview -->
      <div class="neo-browser-body">
        <div class="flex items-center gap-3">
          <h3 class="!text-base !mb-0 font-extrabold text-[#3B1629]">Live Edge Telemetry Dashboard</h3>
          <span class="px-2.5 py-0.5 rounded-full bg-[#D83B78] text-[#FAF5EE] font-mono text-[9px] font-bold">● ONLINE</span>
        </div>

        <div class="grid grid-cols-3 gap-3 my-2">
          <div class="p-3 rounded-2xl bg-[#F6C7D4]/45">
            <div class="font-mono text-[9px] font-bold text-[#D83B78]">THROUGHPUT</div>
            <div class="text-xl font-black text-[#3B1629] my-0.5">4.28M/s</div>
            <div class="font-mono text-[9px] font-bold text-[#D83B78]">+18.4% vs baseline</div>
          </div>
          <div class="p-3 rounded-2xl bg-[#DCECE3]/60">
            <div class="font-mono text-[9px] font-bold text-[#2E8584]">P99 LATENCY</div>
            <div class="text-xl font-black text-[#3B1629] my-0.5">11.4 ms</div>
            <div class="font-mono text-[9px] font-bold text-[#2E8584]">-42.0% lock-free</div>
          </div>
          <div class="p-3 rounded-2xl bg-[#F3E3D3]/60">
            <div class="font-mono text-[9px] font-bold text-[#3B1629]">CACHE HIT</div>
            <div class="text-xl font-black text-[#3B1629] my-0.5">99.42%</div>
            <div class="font-mono text-[9px] font-bold text-[#3B1629]">Edge CRDT active</div>
          </div>
        </div>

        <div class="p-2.5 rounded-xl bg-[#EFECE4]/80 flex justify-between items-center">
          <span class="font-mono text-[9px] font-bold text-[#8C244E]">REAL-TIME FRAME STREAM</span>
          <span class="font-mono text-[9px] font-bold text-[#2E8584]">STATUS: 200 OK (ZERO DROPPED FRAMES)</span>
        </div>
      </div>
    </div>

  </div>
</div>
