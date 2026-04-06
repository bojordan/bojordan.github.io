---
layout: post
title: "ColorIdentity: A Theme-Aware VS Code Extension - Tutorial (WIP)"
---

[ColorIdentity](https://github.com/bojordan/ColorIdentity) is a VS Code extension that gives each workspace a unique color derived from its folder name and your active theme. Inspired by the excellent [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock) extension, but I wanted more control over how colors are generated. Could we do theme-aware tints that adapt automatically rather than picking from a fixed palette? Plus, I wanted to learn how VS Code extensions actually work.

Currently, it just picks foundation colors based on dark/light theme, and then allows hue shift from
there. I will be experimenting with it picking specific elements from your user-specified theme, and attempting to shift from within a color space that is aesthetically appropriate for the overall theme.

A [10-section tutorial](/projects/color-identity/tutorial/) is in progress, covering VS Code extension APIs, HSL color science, deterministic hashing, and a PNG encoder built from scratch. More to come once the tutorial is complete and the extension is hopefully published to the Marketplace.

__Update:__ I've added the "harmonized" mode where it picks colors influenced by your currently active theme. I've also pushed the first build to the [VS Code extensions marketplace](https://marketplace.visualstudio.com/items?itemName=bojordan.color-identity), so go give it a try.

**[Start the Tutorial](/projects/color-identity/tutorial/)**
