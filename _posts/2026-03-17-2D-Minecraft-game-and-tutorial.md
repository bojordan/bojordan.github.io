---
layout: post
title: "Build Your Own 2D Minecraft — A Game and Tutorial"
---

I built a 2D Minecraft clone that runs entirely in the browser — no downloads, no installs, just a single HTML file with JavaScript and canvas rendering.

**[⛏️ Play the Game](/projects/minecraft2d/)**

It's got procedurally generated terrain, mining, building, an inventory system, crafting, a day/night cycle, and more. All in about 800 lines of vanilla JavaScript.

## The Tutorial

More fun than the game itself: I wrote a [12-lesson tutorial](/projects/minecraft2d/tutorial/) that walks through building it from scratch, aimed at a fifth-grade reading level. Each lesson is a self-contained web page with live interactive demos embedded right in the page.

The lessons build progressively:

1. **Hello, Canvas!** — HTML basics and drawing rectangles
2. **Colors & Shapes** — Variables, functions, building a character
3. **The Animation Loop** — The game loop and `requestAnimationFrame`
4. **Keyboard Controls** — Event listeners and WASD movement
5. **Gravity & Jumping** — Velocity, acceleration, physics
6. **A World of Blocks** — 2D arrays and grid rendering
7. **Collision Detection** — Player vs. block collision
8. **Scrolling Camera** — Worlds bigger than the screen
9. **Breaking & Placing Blocks** — Mouse input and world modification
10. **Inventory System** — Collecting items and hotbar management
11. **World Generation** — Noise functions and procedural terrain
12. **The Complete Game** — Day/night, crafting, health, and polish

Every concept is explained with analogies a kid would understand (flip-books for animation, lockers for arrays, light switches for key tracking), and each lesson ends with challenges to encourage experimentation.

**[📚 Start the Tutorial](/projects/minecraft2d/tutorial/)**
