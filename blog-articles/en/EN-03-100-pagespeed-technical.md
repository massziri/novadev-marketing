# How We Hit 100/100 PageSpeed on Every Client Website
**Target keyword:** high performance website agency / premium website development (170–480/mo — Very Low)
**Backlinks:** https://novadev-audit.vercel.app
**Platforms:** dev.to, Hashnode, IndieHackers, Hacker News (Show HN)
**Rule: NO France/French references — technical article for dev community**

---

Performance isn't a premium feature. At [Nova Dev](https://novadev-audit.vercel.app), it's a non-negotiable baseline — every site we ship hits 90+ on PageSpeed Insights. Here's exactly how.

---

## The stack

```
Framework:    Hono (Cloudflare Workers)
Styling:      Tailwind CSS — purged and minified at build
Images:       WebP + lazy loading + explicit dimensions
Deployment:   Cloudflare Pages (edge network, 300+ PoPs)
CDN:          Cloudflare (automatic, global)
Fonts:        system-ui stack — zero font load overhead
Analytics:    Cloudflare Web Analytics (no script overhead)
```

Results:
- **< 1ms cold start** — Cloudflare Workers as V8 isolates, not containers
- **Sub-100ms TTFB** — consistently from any location
- **Zero Node.js overhead** — pure V8 runtime

---

## Why most agency sites underperform

Standard agency workflow → performance problems at every step:
1. WordPress theme + Elementor/Divi
2. 15–25 plugins installed
3. Client images uploaded as-is (3–8MB JPEGs)
4. Deployed to shared hosting at €5/month
5. Caching plugin added, called "optimised"

Result: 60+ HTTP requests, 12MB assets, PageSpeed score of 38.

---

## Our build process

### Step 1: Architecture first
Define communication hierarchy before writing a line of code. Prevents the "add more" trap.

### Step 2: Hono edge application

```typescript
import { Hono } from 'hono'
import { serveStatic } from 'hono/cloudflare-workers'
import { compress } from 'hono/compress'

const app = new Hono()
app.use('*', compress()) // Brotli/gzip on all responses
app.use('/static/*', serveStatic({ root: './' }))
app.get('/', (c) => c.html(renderPage(), 200, {
  'Cache-Control': 'public, max-age=3600, stale-while-revalidate=86400'
}))

export default app
```

### Step 3: CSS that weighs almost nothing

```bash
# Development: ~2.8MB (full Tailwind)
# After PurgeCSS: ~11KB
# After Brotli: ~3.1KB
```

### Step 4: Image pipeline

```bash
cwebp -q 82 input.jpg -o output.webp                     # 3.2MB → 94KB
cwebp -q 82 -resize 800 0 input.jpg -o output-800w.webp  # Mobile variant
```

```html
<picture>
  <source srcset="/img/hero-1200w.webp 1200w, /img/hero-800w.webp 800w"
          sizes="(max-width: 768px) 100vw, 50vw" type="image/webp">
  <img src="/img/hero-fallback.jpg" alt="..." width="1200" height="675"
       loading="lazy" decoding="async">
</picture>
```

Explicit `width` + `height` → eliminates CLS (Cumulative Layout Shift).

### Step 5: Critical CSS inlined

```html
<style>/* ~800 bytes of above-fold styles inlined */</style>
<link rel="preload" href="/static/styles.min.css" as="style"
      onload="this.onload=null;this.rel='stylesheet'">
```

### Step 6: Deploy to Cloudflare Pages

```bash
npm run build && npx wrangler pages deploy dist --project-name client-site
# ✓ Deployed globally in ~15 seconds
```

---

## Typical results

| Metric | Target | Result |
|--------|--------|--------|
| Performance | 90+ | **98–100** |
| Accessibility | 90+ | **95–100** |
| Best Practices | 90+ | **100** |
| SEO | 90+ | **100** |
| LCP | < 2.5s | **0.7–1.1s** |
| CLS | < 0.1 | **0.00** |

---

## Business impact

- Google ranking — performance is a documented ranking factor since 2021
- Bounce rate — under 1s load time = 3× lower bounce than 5s sites
- Conversions — 1-second improvement → 2–3% conversion rate increase

---

## Pricing

Our **Growth package** delivers everything above — for $400 / £400 / €400. Up to 12 pages, premium UI, 100/100 PageSpeed guaranteed, advanced SEO, mobile-first, 3 revision rounds.

**[Start your project →](https://novadev-audit.vercel.app)** | **[Free audit first →](https://novadev-audit.vercel.app)**

---
**Tags:** #webdev #performance #cloudflare #hono #pagespeed #webperf #frontend
