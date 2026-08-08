# Boostie Scroll Engine

Boostie Engine v5.1 — a lightweight browser performance engine focused on smoother scrolling, efficient rendering, and safe DOM optimization.


## Installation
Add Boostie to your <head>:

<pre> <head><script
  src="https://cdn.jsdelivr.net/gh/FoxLangTM/Boostie-scroll-engine@main/boostie.min.js"
  defer
></script></head> </pre>

<pre>
Boostie starts automatically when the page is ready.


## Features
- Adaptive Virtual Scroll
- LRU memory driver
- CPU / frame monitoring
- Web Worker pool
- Native lazy loading
- Safe same-origin prefetching
- Adaptive performance modes
- Visibility-aware rendering
- Optional comment cleanup
- Runtime diagnostics
- Priority-based task scheduler


## Virtual Scroll:
Virtual scrolling is opt-in and only affects explicitly marked elements.

<pre data-boostie-virtual>
Very large text content...
</pre>

Virtual Scroll is enabled automatically for blocks containing 200+ lines.

Boostie renders only the required portion of large text blocks while keeping the original content available.


##Diagnostics
Access the Boostie API through:

window.__BOOSTIE__
Get a complete performance report:
window.__BOOSTIE__.getReport();
Virtual Scroll statistics:
window.__BOOSTIE_VIRTUAL_SCROLL__.getStats();
CPU statistics:
window.__BOOSTIE_CPU_MONITOR__.getStats();


## Performance
Boostie automatically adapts Virtual Scroll based on frame performance:

- "performance"
- "balanced"
- "emergency"

It also detects slow connections and low battery conditions to reduce unnecessary prefetching.


## Design
Boostie is designed to be safe by default:

- No automatic virtualization of every <> "pre" or "code"
- Existing content is preserved
- Existing "contenteditable" elements are not modified
- Same-origin prefetch only
- Optional features remain disabled unless explicitly enabled
</pre>



### Version
Boostie Engine v5.1
«Safe performance optimization without unnecessary DOM interference.»