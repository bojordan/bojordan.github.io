---
layout: post
title: "Building a Spectrum Analyzer for iPhone - A Tutorial"
---

Fifteen years ago I built iPhone apps for a short while. Objective-C, UIKit, Xcode 3. Then, I got a new job and ended up never giving myself permission to devote any time to the Apple plaform.

Long before that, I had brief hopes of getting into music software engineering. That story is for another day, but for at least two years I've wanted to write my own tuner app for guitars and violins. I thought this would be reasonable project and a good excuse to learn Swift. But, I've never made time.

Now, we have powerful creation tools available to scratch itches. Time is less of a limiting factor. But, in keeping with a new theme, I also care deeping about these creation tools being powerful _educators_, and not just _producers_.

The result is a small Swift/SwiftUI app -- and, most importantly, tutorial -- that does real-time FFT analysis and displays 48 animated frequency bars with musical note detection. Four files, about 200 lines of code. It runs on an iPhone and it feels like magic when you sing into it and watch the bars dance. There will also be a Mac verison, because I need to tune guitars at my desk, too. And, in the near future, I hope my wife and kids will be able to use it on their amazing journeys with the violin.

### The tutorial

I wrote up the whole process as an [11-section tutorial](/projects/spectrum-analyzer/tutorial/) aimed at programmers like me — people who know how to code but have never touched Swift, SwiftUI, or digital signal processing.

It runs on two parallel tracks: iOS development and audio/DSP theory. Each theory section arrives right before the code that implements it, so you're never reading about something abstract — you're about to use it.

The sections:

0. [**Preface & Orientation**](/projects/spectrum-analyzer/tutorial/section00) - What you'll build, C# to Swift quick reference
1. [**Your First iOS App**](/projects/spectrum-analyzer/tutorial/section01) - Xcode project, SwiftUI fundamentals
2. [**What Is Sound?**](/projects/spectrum-analyzer/tutorial/section02) - Sampling, PCM, Nyquist, RMS, decibels
3. [**Capturing Audio on iOS**](/projects/spectrum-analyzer/tutorial/section03) - AVAudioEngine, mic permissions, a working VU meter
4. [**Accelerating the Math**](/projects/spectrum-analyzer/tutorial/section04) - Apple's Accelerate/vDSP framework
5. [**The Fourier Transform**](/projects/spectrum-analyzer/tutorial/section05) - FFT intuition, frequency bins, window functions
6. [**Building the Spectrum Analyzer**](/projects/spectrum-analyzer/tutorial/section06) - The SpectrumAnalyzer struct, log-spaced bars, note detection
7. [**The Spectrum UI**](/projects/spectrum-analyzer/tutorial/section07) - SpectrumView component, dark theme, final ContentView
8. [**Running on Your iPhone**](/projects/spectrum-analyzer/tutorial/section08) - Device setup, provisioning, debugging audio
9. [**Beyond the Tutorial**](/projects/spectrum-analyzer/tutorial/section09) - TestFlight, App Store, better pitch detection
10. [**Complete Source Code**](/projects/spectrum-analyzer/tutorial/section10) - All four final files with cross-references

By the end of Section 3 you have a working VU meter. By the end of Section 7 you have the full spectrum analyzer. The last three sections cover getting it onto a real device and where to go next.

### How it was built

Like the [2D Minecraft tutorial](/projects/minecraft2d/tutorial/), this was built with AI coding tools — this one was specifically with Claude Code. The app itself came out of a conversation where I was learning, asking questions, and iterating. The tutorial came afterward, distilling that learning journey into something structured.

The interesting thing about using AI for this wasn't the code generation, and it wasn't just the conversation. It's the opportunity to capture the conversation as a design for sharing the knowledge. And, for me, for retaining the knowledge and expertise. If you don't know how the tools need to build something, you're going to be a terrible shepherd in the future.

I'm still not sure whether I'm "back" to iOS development or just visiting. But I learned more in a weekend than I expected to, and I have a working app that makes sound visible. That's a good start.

**[Start the Tutorial](/projects/spectrum-analyzer/tutorial/)**
