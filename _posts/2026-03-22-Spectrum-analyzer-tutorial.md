---
layout: post
title: "Building an Audio Spectrum Analyzer for iPhone - A Tutorial"
---

Fifteen years ago I built iPhone apps for a short while. Objective-C, UIKit, Xcode 3. Then, I got a new job and ended up never giving myself permission to devote any time to the Apple plaform.

Long before that, I had brief hopes of getting into music software engineering. That story is for another day, but for at least two years I've wanted to write my own tuner app for guitars and violins. I thought this would be reasonable project and a good excuse to learn Swift. But, I've never made time.

Now, we have powerful creation tools available to scratch itches. Time is less of a limiting factor. But, in keeping with a new theme, I also care deeply about these creation tools being powerful _educators_, and not just _producers_.

The result is a small Swift/SwiftUI app -- and, most importantly, tutorial -- that does real-time FFT analysis and displays 48 animated frequency bars with musical note detection. Four files, about 200 lines of code. It runs on an iPhone and it feels like magic when you sing into it and watch the bars dance. There will also be a Mac verison, because I need to tune guitars at my desk, too. And, in the near future, I hope my wife and kids will be able to use it on their amazing journeys with the violin.

### The tutorial

I wrote up the whole process as an [11-section tutorial](/projects/spectrum-analyzer/tutorial/) aimed at programmers like me — people who know how to code but have never touched Swift, SwiftUI, or digital signal processing.

It runs on two parallel tracks: iOS development and audio/DSP theory. Each theory section arrives right before the code that implements it, so you're never reading about something abstract — you're about to use it.

The sections:

<ol start="0">
<li><a href="/projects/spectrum-analyzer/tutorial/section00"><strong>Preface &amp; Orientation</strong></a> - What you'll build, C# to Swift quick reference</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section01"><strong>Your First iOS App</strong></a> - Xcode project, SwiftUI fundamentals</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section02"><strong>What Is Sound?</strong></a> - Sampling, PCM, Nyquist, RMS, decibels</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section03"><strong>Capturing Audio on iOS</strong></a> - AVAudioEngine, mic permissions, a working VU meter</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section04"><strong>Accelerating the Math</strong></a> - Apple's Accelerate/vDSP framework</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section05"><strong>The Fourier Transform</strong></a> - FFT intuition, frequency bins, window functions</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section06"><strong>Building the Spectrum Analyzer</strong></a> - The SpectrumAnalyzer struct, log-spaced bars, note detection</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section07"><strong>The Spectrum UI</strong></a> - SpectrumView component, dark theme, final ContentView</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section08"><strong>Running on Your iPhone</strong></a> - Device setup, provisioning, debugging audio</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section09"><strong>Beyond the Tutorial</strong></a> - TestFlight, App Store, better pitch detection</li>
<li><a href="/projects/spectrum-analyzer/tutorial/section10"><strong>Complete Source Code</strong></a> - All four final files with cross-references</li>
</ol>

By the end of Section 3 you have a working VU meter. By the end of Section 7 you have the full spectrum analyzer. The last three sections cover getting it onto a real device and where to go next.

### How it was built

Like the [2D Minecraft tutorial](/projects/minecraft2d/tutorial/), this was built with AI coding tools — this one was specifically with Claude Code. The app itself came out of a conversation where I was learning, asking questions, and iterating. The tutorial came afterward, distilling that learning journey into something structured.

The interesting thing about using AI for this wasn't the code generation, and it wasn't just the conversation. It's the opportunity to capture the conversation as a design for sharing the knowledge. And, for me, for retaining the knowledge and expertise. If you don't know how the tools need to build something, you're going to be a terrible shepherd in the future.

I'm still not sure whether I'm "back" to iOS development or just visiting. But I learned more in a weekend than I expected to, and I have a working app that makes sound visible. That's a good start.

**[Start the Tutorial](/projects/spectrum-analyzer/tutorial/)**
