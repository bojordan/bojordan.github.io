by---
layout: post
title: "Theming Microsoft Teams from the Outside - An Observation-First Tutorial"
---

Microsoft Teams supports exactly three built-in themes: Light, Dark, and High Contrast. There&rsquo;s no custom theme API. But new Teams runs on WebView2 (Chromium), which exposes the Chrome DevTools Protocol &mdash; and that means an external Node.js process can connect via CDP, inspect the running UI, and inject CSS that overrides Fluent UI&rsquo;s 400+ design tokens.

Theme Injector is a tool that does exactly this. The interesting part isn&rsquo;t the injection itself (that&rsquo;s a `<style>` element) — it&rsquo;s the *observation-first methodology* that makes the theming robust: extract every token from the live app, analyze the design system structure, verify visually, and only then generate overrides algorithmically.

This was written up as a [7-section tutorial](/projects/theme-injector/tutorial/) covering CDP internals, Fluent UI token systems, color science for polarity-aware dimming, automated VS Code theme porting, and the challenges of theming calling screens with live video feeds.

**[Start the Tutorial](/projects/theme-injector/tutorial/)**
