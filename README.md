# Apartments Anita

Complete static HR/EN website. Open index.html, or serve this directory using any static server. No build step, framework, package installation or API key is needed.

## Files and deployment

- index.html: page markup, CSS and JavaScript.
- assets/: responsive local WebP photographs.
- img1.jpg–img35.jpg: preserved originals.
- IMAGE-MAP.md: complete visual inventory and placement rationale.
- qa/: inspection screenshots and breakpoint results; not required for deployment.

For GitHub Pages or Vercel, deploy index.html and assets/ together at the site root. Vercel framework preset: Other; no build command. This task did not publish the site. After choosing a production domain, use its absolute URL for og:image and add a canonical URL; no domain was invented.

## What is implemented

Croatian default; English interface and content; localStorage preference; semantic sections; responsive navigation; mobile booking bar; curated photo grid; native modal gallery with 35 photos, keyboard arrows, Escape, focus return and swipe; on-demand Google map; verified Booking.com links; descriptive alt text; reduced-motion support; lazy-loaded responsive images; SEO, Open Graph and factual LodgingBusiness JSON-LD. No invented units, prices, testimonials, contacts or booking engine. The supplied 9.2/151 rating is explicitly marked as reference information.

## Verification actually performed

- Rendered and visually inspected in headless Google Chrome using Playwright.
- Tested widths 375, 390, 430, 768, 1024 and 1440 in both HR and EN: zero document horizontal overflow, missing text translation keys or broken anchor targets.
- Tested HR/EN persistence after reload, mobile menu open/close, gallery next/previous and wraparound, Escape, focus return and scroll unlocking.
- Swipe handler tested with simulated touch events, not on a physical device.
- Decoded all 35 full-size gallery images and verified all 70 optimized image paths return HTTP 200.
- No page JavaScript errors recorded.
- axe-core WCAG 2 A/AA and 2.1 AA checks: zero violations on the settled desktop, mobile and open-dialog views. Automated checks do not constitute a complete accessibility certification.
- Booking.com identity and address matched through web search. HR and EN CTA destinations verified in the rendered DOM.
- Google map toggle, address query and language parameter tested; external map rendering was blocked by the environment network. Direct Google Maps link is included.
- Lighthouse not run; no Lighthouse scores are claimed.

## Remaining external checks

No known incomplete local interactions. Check the external map on the deployed domain, confirm the final domain metadata, and run deployed Lighthouse and a real iOS/Android touch check. Photos are limited by the supplied source resolution (at most 1024px wide); they were not artificially enlarged or replaced.
