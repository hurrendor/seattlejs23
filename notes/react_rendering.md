---
id: clnwkhztghgqen05w4dorjn
title: React_rendering
desc: ''
updated: 1691516566034
created: 1691514884910
---
# 50 shades of React rendering with Next.js - Ben Ilegbodu

[Blog post](https://slides.benmvp.com/2023/seattlejs/nextjs.html#/)

[Slides](https://slides.benmvp.com/2023/seattlejs/nextjs.html#/)

## About React
Multiple renderers

Next.js uses rendering React to a string instead of to a DOM (isomorphic React) [circa 2016]

Types of Rendering

Next focuses on path based routing, dyanmic path based routing
//src/pages/product/[id].tsx

## Client-Side Rendering (CSR)
Page HTML is rendered in the browser. Great for consistently changing data, or dynamic content and provides a fast response time.

Great for dashboards && 3rd party widgets, or usage of 3rd party widgets.

Cons:
- Slow render time
- Poor SEO && UI cache

## Server-Side Rendering (SSR) 
AKA 'Dyanmic Rendering'
Page HTML is generated on the server for every request. Fast render times, great for SEO. Great for tailored data.

Cons:
- Slow response times

## Static-site generation (SSG)
Page HTML is pre-rendered at build time
Great for pages that don't need any tailored or dynamic data; anything that would be cacheable and usable as a CDN. Blog posts, marketing pages, static product listings etc.

Cons:
- Slow build times
- No dynamic or user-specific content

Example given uses the `fallback` property in Next.js
[TODO: Read up on fallback property](https://slides.benmvp.com/2023/seattlejs/nextjs.html#/)

Suggestions for SSG on cacheable components and using dyanmic to retrieve dynamic data.

## Incremental Static Regeneration (ISR)
Page HTML is regenerated on the server after cache timeout. Creates fast initial load times but also allows for frequent data updates. 

Cons:
- Slow build time
- Not a ton of ability for dynamic data

Takeaway: Utilize the different render modes as they make sense for your product or pages. Audit your site to optimize for user experience.