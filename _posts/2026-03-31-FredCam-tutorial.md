---
layout: post
title: "FredCam: A 3D Printer Camera Viewer for iOS - A Tutorial"
---

Fred is our Bambu Lab P2S 3D printer, and we don't like having to run Bambu Handy just to see the camera. How could we _not_ throw Claude Code at the problem to get a tidy little app - and a programming lesson - both at the same time?

[FredCam](https://github.com/bojordan/FredCam) is a small iOS/iPadOS app that streams the printer's camera over the local network. The interesting part is that the stream is RTSPS — RTSP over TLS — with a self-signed certificate, which turns out to be surprisingly hard to connect to with standard iOS tooling. AVPlayer won't bypass certificate validation. One solution is [KSPlayer](https://github.com/kingslay/KSPlayer), which wraps FFmpeg and exposes its `tls_verify: 0` option.

Six Swift files, about 650 lines of code.

### The tutorial

The interesting thing about building this wasn't just making the stream work — it was everything around it: choosing the right dependency, understanding what you're signing up for license-wise, bridging UIKit into SwiftUI, modeling app state cleanly. The app is small but dense with real-world decisions.

This was written up as a [10-section tutorial](/projects/fredcam/tutorial/) aimed at programmers who know how to code but haven't spent much time in Swift or iOS.

The sections:

<ol start="0">
<li><a href="/projects/fredcam/tutorial/section00"><strong>Preface &amp; Orientation</strong></a> — What FredCam is, what you'll learn, the six-file map</li>
<li><a href="/projects/fredcam/tutorial/section01"><strong>The RTSPS Problem</strong></a> — RTSP, TLS, self-signed certs, and why standard players fail</li>
<li><a href="/projects/fredcam/tutorial/section02"><strong>XcodeGen and Swift Package Manager</strong></a> — Code-first project definition, SPM dependency resolution</li>
<li><a href="/projects/fredcam/tutorial/section03"><strong>KSPlayer — Dependencies and Licenses</strong></a> — GPL v3, FFmpeg's LGPL, what open-source licenses mean for your iOS app</li>
<li><a href="/projects/fredcam/tutorial/section04"><strong>Data Model and Persistent Settings</strong></a> — ObservableObject, @Published, UserDefaults</li>
<li><a href="/projects/fredcam/tutorial/section05"><strong>App State — The StreamState Machine</strong></a> — Enum-driven state machines, @StateObject, @Binding</li>
<li><a href="/projects/fredcam/tutorial/section06"><strong>Bridging UIKit and SwiftUI</strong></a> — UIViewRepresentable, the Coordinator pattern, delegate callbacks</li>
<li><a href="/projects/fredcam/tutorial/section07"><strong>Low-Latency Streaming Options</strong></a> — KSPlayer/FFmpeg avOptions, TCP transport, buffering tradeoffs</li>
<li><a href="/projects/fredcam/tutorial/section08"><strong>Adaptive Layout, PiP, and System Permissions</strong></a> — verticalSizeClass, stable view identity, Picture-in-Picture, Info.plist</li>
<li><a href="/projects/fredcam/tutorial/section09"><strong>Future Directions and License Considerations</strong></a> — Distribution concerns, alternatives to KSPlayer, what to fix before shipping</li>
</ol>

Section 3 on licenses ended up being one of the more interesting parts to write. Claude initially assumed KSPlayer was MIT-licensed — it's not, it's GPL v3, which is _very_ different. (Bad Claude!) That's a significant difference if you ever want to distribute the app, and it changes the analysis of what you're committing to when you take the dependency. For personal use, no issue. For anything you want to ship to others, you have real choices to make.

### How it was built

Built with Claude Code, same as the [spectrum analyzer](/projects/spectrum-analyzer/tutorial/) and [Minecraft tutorial](/projects/minecraft2d/tutorial/). The app came first — a focused session of asking questions, making decisions, and iterating. The tutorial came after, as a way of organizing and sharing what the process surfaced.

### Why do this?

I'm making these tutorials - or, perhaps, I should say I'm having them made. Regardless, I'm _reading_ them myself. Maybe I won't be the only one learning something here, and hopefully I'm still learning a bit more than just how to craft prompts. I still want to believe these are tools for learning as much as for producing. Building is more fun when it's a learning process, isn't it?

**[Start the Tutorial](/projects/fredcam/tutorial/)**
